# 如何かのSHIORIイベント実装状況

各イベントの定義は原則[UKADOC](http://ssp.shillest.net/ukadoc/manual/list_shiori_event.html)のSSPの動作に準拠します。

ただし全てのイベントで「パス」は通知されません。

打ち消し線のある項目は、実装予定はあるが未実装であることを示します。

ここに存在しないイベントは実装されないことを意味しないが、優先度は低いはずです。

またここに存在したとしても、バグ等で正しく送信されていない場合があるので、そのような場合は報告してください。

## 起動・終了・切り替えイベント

- OnFirstBoot
- OnBoot
- OnClose
- OnCloseAll
- OnGhostChanged
- OnGhostChanging
- OnGhostCalled
- OnGhostCalling
- OnGhostCallComplete
- OnOtherGhostBooted
- OnOtherGhostChanged
- OnOtherGhostClosed
- <del>OnShellChanged</del>
- <del>OnShellChanging</del>
- <del>OnDressupChanged</del>
- <del>OnBalloonChange</del>

以下は実装予定なし

- OnCacheSuspend
- OnCacheRestore
- OnInitialize
- OnDestroy
- OnSysResume
- OnSysSuspend

## 入力ボックスイベント

- <del>OnTeachStart</del>
- <del>OnTeachInputCancel</del>
- <del>OnTeach</del>
- OnCommunicate
- OnCommunicateInputCancel
- OnUserInput
- OnUserInputCancel
- <del>inputbox.autocomplete</del>

## ダイアログボックスイベント

実装なし

## 時間イベント

- OnSecondChange
- OnMinuteChange

## 消滅イベント

- <del>OnVanishSelecting</del>
- <del>OnVanishSelected</del>
- <del>OnVanishCancel</del>
- <del>OnVanishButtonHold</del>
- <del>OnVanished</del> SSPが行うOnOtherGhostVanishからのフォールバックは行わない。
- <del>OnOtherGhostVanish</del>

## 選択肢イベント

- OnChoiceSelect
- OnChoiceSelectEx
- <del>OnChoiceEnter</del>
- <del>OnChoiceTimeout</del>
- <del>OnChoiceHover</del>
- OnAnchorSelect
- OnAnchorSelectEx

## サーフェスイベント

- <del>OnSurfaceChange</del>
- <del>OnSurfaceRestore</del>

## マウスイベント

- OnMouseClick
- <del>OnMouseClickEx</del>
- OnMouseDoubleClick
- <del>OnMouseDoubleClickEx</del>
- <del>OnMouseMultipleClick</del>
- <del>OnMouseMultipleClickEx</del>
- OnMouseUp
- <del>OnMouseUpEx</del>
- OnMouseDown
- <del>OnMouseDownEx</del>
- OnMouseMove
- OnMouseWheel
- <del>OnMouseEnterAll</del>
- <del>OnMouseLeaveAll</del>
- <del>OnMouseEnter</del>
- <del>OnMouseLeave</del>
- <del>OnMouseDragStart</del>
- <del>OnMouseDragEnd</del>
- <del>OnMouseHover</del>

## バルーンイベント

- <del>OnBalloonBreak</del>
- <del>OnBalloonClose</del>
- <del>OnBalloonTimeout</del>

## トレイバルーンイベント

実装なし

## インストールイベント

- <del>OnInstallBegin</del>
- <del>OnInstallComplete</del>
- <del>OnInstallCompleteEx</del>
- <del>OnInstallFailure</del>
- <del>OnInstallRefuse</del>

## ファイルドロップイベント

実装なし

## URLドロップイベント

実装なし

## ネットワーク更新イベント

実装なし

## 時計合わせイベント

実装予定なし

## メールチェックイベント

実装予定なし

## ヘッドラインセンスイベント

実装なし

## カレンダーイベント

実装予定なし

## SSTPイベント

実装なし

## その他通信イベント

実装予定なし

## イベント送信失敗イベント

実装なし

## 見切れ・重なりイベント

実装なし

## ネットワーク状態イベント

実装なし

## スクリーン状態イベント

実装予定なし

## バッテリー状態イベント

実装なし

## デバイス状態イベント

実装予定なし

## 選択領域モードイベント

実装なし

## 単体イベント

- <del>OnKeyPress</del>
- <del>OnRecommendsiteChoice</del>
- <del>OnTranslate</del>
- <del>OnAITalk</del>
- <del>OnOtherGhostTalk</del>
- <del>OnSoundStop</del>
- <del>OnTextDrop</del>
- <del>OnShellScaling</del>

以下は実装予定なし

- OnEmbryoExist
- OnNekodorifExist

## Notifyイベント

- basewareversion
- <del>uniqueid
- ownerghostname
- otherghostname
- installedghostname
- installedshellname
- installedballoonname
- <del>installedheadlinename</del>
- <del>installedplugin</del>
- <del>ghostpathlist</del>
- <del>balloonpathlist</del>
- <del>headlinepathlist</del>
- <del>pluginpathlist</del>
- <del>rateofusegraph</del>
- OnNotifySelfInfo
- OnNotifyBalloonInfo
- OnNotifyShellInfo
- <del>OnNotifyDressupInfo</del>
- <del>OnNotifyUserInfo</del>
- <del>OnNotifyOSInfo</del>
- <del>OnNotifyFontInfo</del>
- OnNotifyBrowserInfo 独自イベント

以下は実装予定なし

- hwnd
- capability
- calendarskinpathlist
- calendarpluginpathlist
