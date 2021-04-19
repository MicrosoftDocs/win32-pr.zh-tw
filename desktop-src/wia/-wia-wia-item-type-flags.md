---
description: 下列常數會指定 Windows 映像取得 (WIA) 專案類型。
ms.assetid: 7961f692-088a-4f3b-84e9-5fabb0373c3c
title: 'WIA 專案類型旗標 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaItemTypeAnalyze
- WiaItemTypeAudio
- WiaItemTypeBurst
- WiaItemTypeDeleted
- WiaItemTypeDevice
- WiaItemTypeDisconnected
- WiaItemTypeDocument
- WiaItemTypeFile
- WiaItemTypeFolder
- WiaItemTypeFree
- WiaItemTypeGenerated
- WiaItemTypeHasAttachments
- WiaItemTypeHPanorama
- WiaItemTypeImage
- WiaItemTypeProgrammableDataSource
- WiaItemTypeRemoved
- WiaItemTypeRoot
- WiaItemTypeStorage
- WiaItemTypeTransfer
- WiaItemTypeTwainCapabilityPassThrough
- WiaItemTypeVideo
- WiaItemTypeVPanorama
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: c5b7a9e6108825205b2d8bc5ab40ce8096e32ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973074"
---
# <a name="wia-item-type-flags"></a>WIA 專案類型旗標

下列常數會指定 Windows 映像取得 (WIA) 專案類型。



| 常數                                                                                                                                                                                                                                                                                     | 描述                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WiaItemTypeAnalyze"></span><span id="wiaitemtypeanalyze"></span><span id="WIAITEMTYPEANALYZE"></span><dl> <dt>**WiaItemTypeAnalyze**</dt> </dl>                                                                             | 此專案支援 [**IWiaItem：： AnalyzeItem**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem) 方法。 *不支援這個常數* Windows Vista （含） *以後版本。*<br/>                                                                                                                               |
| <span id="WiaItemTypeAudio"></span><span id="wiaitemtypeaudio"></span><span id="WIAITEMTYPEAUDIO"></span><dl> <dt>**WiaItemTypeAudio**</dt> </dl>                                                                                     | 專案是音訊檔案。 僅對同時具有 **WiaItemTypeFile** 屬性的專案有效。 <br/>                                                                                                                                                                                     |
| <span id="WiaItemTypeBurst"></span><span id="wiaitemtypeburst"></span><span id="WIAITEMTYPEBURST"></span><dl> <dt>**WiaItemTypeBurst**</dt> </dl>                                                                                     | 僅適用于資料夾。 此資料夾中的影像是以連續的時間順序拍攝。 *不支援這個常數* Windows Vista （含） *以後版本。*<br/>                                                                                                                                       |
| <span id="WiaItemTypeDeleted"></span><span id="wiaitemtypedeleted"></span><span id="WIAITEMTYPEDELETED"></span><dl> <dt>**WiaItemTypeDeleted**</dt> </dl>                                                                             | 專案會從樹狀結構標示為已刪除。 <br/>                                                                                                                                                                                                                                          |
| <span id="WiaItemTypeDevice"></span><span id="wiaitemtypedevice"></span><span id="WIAITEMTYPEDEVICE"></span><dl> <dt>**WiaItemTypeDevice**</dt> </dl>                                                                                 | 專案代表連線的裝置。 <br/>                                                                                                                                                                                                                                               |
| <span id="WiaItemTypeDisconnected"></span><span id="wiaitemtypedisconnected"></span><span id="WIAITEMTYPEDISCONNECTED"></span><dl> <dt>**WiaItemTypeDisconnected**</dt> </dl>                                                         | 專案代表已中斷連線的裝置。 <br/>                                                                                                                                                                                                                                            |
| <span id="WiaItemTypeDocument"></span><span id="wiaitemtypedocument"></span><span id="WIAITEMTYPEDOCUMENT"></span><dl> <dt>**WiaItemTypeDocument**</dt> </dl>                                                                         | 代表檔的專案。 *只有下列情況才支援這個常數：* Windows Vista （含） *以後版本。*<br/>                                                                                                                                                                                        |
| <span id="WiaItemTypeFile"></span><span id="wiaitemtypefile"></span><span id="WIAITEMTYPEFILE"></span><dl> <dt>**WiaItemTypeFile**</dt> </dl>                                                                                         | 專案是檔案。 <br/>                                                                                                                                                                                                                                                                   |
| <span id="WiaItemTypeFolder"></span><span id="wiaitemtypefolder"></span><span id="WIAITEMTYPEFOLDER"></span><dl> <dt>**WiaItemTypeFolder**</dt> </dl>                                                                                 | 專案是資料夾。 <br/>                                                                                                                                                                                                                                                                 |
| <span id="WiaItemTypeFree"></span><span id="wiaitemtypefree"></span><span id="WIAITEMTYPEFREE"></span><dl> <dt>**WiaItemTypeFree**</dt> </dl>                                                                                         | 專案未初始化或已刪除。 <br/>                                                                                                                                                                                                                                        |
| <span id="WiaItemTypeGenerated"></span><span id="wiaitemtypegenerated"></span><span id="WIAITEMTYPEGENERATED"></span><dl> <dt>**WiaItemTypeGenerated**</dt> </dl>                                                                     | 此專案是由應用程式或驅動程式所建立，而且在驅動程式專案樹狀結構中沒有對應的專案。 <br/>                                                                                                                                                               |
| <span id="WiaItemTypeHasAttachments"></span><span id="wiaitemtypehasattachments"></span><span id="WIAITEMTYPEHASATTACHMENTS"></span><dl> <dt>**WiaItemTypeHasAttachments**</dt> </dl>                                                 | 專案具有檔案附件。 *不支援這個常數* Windows Vista （含） *以後版本。*<br/>                                                                                                                                                                                          |
| <span id="WiaItemTypeHPanorama"></span><span id="wiaitemtypehpanorama"></span><span id="WIAITEMTYPEHPANORAMA"></span><dl> <dt>**WiaItemTypeHPanorama**</dt> </dl>                                                                     | 專案代表水準全景影像。 *不支援這個常數* Windows Vista （含） *以後版本。*<br/>                                                                                                                                                                       |
| <span id="WiaItemTypeImage"></span><span id="wiaitemtypeimage"></span><span id="WIAITEMTYPEIMAGE"></span><dl> <dt>**WiaItemTypeImage**</dt> </dl>                                                                                     | 專案是影像檔案。 僅對同時具有 **WiaItemTypeFile** 屬性的專案有效。 <br/>                                                                                                                                                                                     |
| <span id="WiaItemTypeProgrammableDataSource"></span><span id="wiaitemtypeprogrammabledatasource"></span><span id="WIAITEMTYPEPROGRAMMABLEDATASOURCE"></span><dl> <dt>**WiaItemTypeProgrammableDataSource**</dt> </dl>                 | 專案代表可程式化的資料來源。 *只有下列情況才支援這個常數：* Windows Vista （含） *以後版本。*<br/>                                                                                                                                                                        |
| <span id="WiaItemTypeRemoved"></span><span id="wiaitemtyperemoved"></span><span id="WIAITEMTYPEREMOVED"></span><dl> <dt>**WiaItemTypeRemoved**</dt> </dl>                                                                             | 已從裝置移除該專案。 <br/>                                                                                                                                                                                                                                            |
| <span id="WiaItemTypeRoot"></span><span id="wiaitemtyperoot"></span><span id="WIAITEMTYPEROOT"></span><dl> <dt>**WiaItemTypeRoot**</dt> </dl>                                                                                         | 識別裝置的專案物件樹狀結構中的根專案。 *只有下列情況才支援這個常數：* Windows Vista （含） *以後版本。*<br/>                                                                                                                                                         |
| <span id="WiaItemTypeStorage"></span><span id="wiaitemtypestorage"></span><span id="WIAITEMTYPESTORAGE"></span><dl> <dt>**WiaItemTypeStorage**</dt> </dl>                                                                             | 專案代表儲存體媒體。 <br/>                                                                                                                                                                                                                                                 |
| <span id="WiaItemTypeTransfer"></span><span id="wiaitemtypetransfer"></span><span id="WIAITEMTYPETRANSFER"></span><dl> <dt>**WiaItemTypeTransfer**</dt> </dl>                                                                         | 可以傳送專案。 <br/>                                                                                                                                                                                                                                                          |
| <span id="WiaItemTypeTwainCapabilityPassThrough"></span><span id="wiaitemtypetwaincapabilitypassthrough"></span><span id="WIAITEMTYPETWAINCAPABILITYPASSTHROUGH"></span><dl> <dt>**WiaItemTypeTwainCapabilityPassThrough**</dt> </dl> | 這種類型表示 WIA 裝置能夠接收來自 TWAIN 相容性層的 TWAIN 功能資料。 如果設定此型別，在 TWAIN 會話期間，由 TWAIN 相容性層所不了解的任何 TWAIN 功能都會傳遞至 WIA 驅動程式。 <br/> |
| <span id="WiaItemTypeVideo"></span><span id="wiaitemtypevideo"></span><span id="WIAITEMTYPEVIDEO"></span><dl> <dt>**WiaItemTypeVideo**</dt> </dl>                                                                                     | 專案代表串流處理影片。 *這兩個常數都不支援* Windows Server 2003 *、* windows Vista *或更新版本。*<br/>                                                                                                                                                      |
| <span id="WiaItemTypeVPanorama"></span><span id="wiaitemtypevpanorama"></span><span id="WIAITEMTYPEVPANORAMA"></span><dl> <dt>**WiaItemTypeVPanorama**</dt> </dl>                                                                     | 專案表示垂直全景影像。 *不支援這個常數* Windows Vista （含） *以後版本。*<br/>                                                                                                                                                                         |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wiadef。h</dt> </dl> |



 

 




