DockPanel Suite (MCS Fork)
==========================

This is the [Promicron](https://www.promicron.de) fork of [DockPanelSuite](https://github.com/dockpanelsuite/dockpanelsuite), used in the MCS (Microscope Control Software) product.

## Branch: `mcs/3.0.4`

Based on upstream `Release_3.0.4` with the following fixes:

- **DockContentHandler**: Dispose `TabPageContextMenuStrip` to prevent memory leak; fix AutoHide pane activation when `ActiveAutoHideContent` is null; disable `bRestoreFocus` `Activate()` call that causes unwanted MDI child activation
- **DockPanel.AutoHideWindow**: Add try/catch in `SetTimerMouseTrack` to prevent unhandled exceptions
- **DockPanel**: Call `DockPanelTheme.CleanUp()` during disposal to release theme resources
- **ThemeBase**: Prevent duplicate ToolStrip registration; subscribe to `Disposed` event to clean up `_stripBefore` dictionary
- **VisualStudioToolStripExtender**: Subscribe to `ToolStrip.Disposed` to remove entries from strips dictionary
- **VS2013SplitterControl**: Add try/catch in `OnPaint`; remove `Debug.Assert` for SplitterSize

## Upstream

For the original project, see [dockpanelsuite/dockpanelsuite](https://github.com/dockpanelsuite/dockpanelsuite).
