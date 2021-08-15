---
description: Windows影像取得 (WIA) 硬體裝置會表示為專案物件的階層樹狀結構。 此樹狀結構中的根專案代表裝置本身，而子專案代表影像、資料夾或掃描張床。
ms.assetid: 240557d6-665e-4879-8c6e-f564ca61e031
title: Item 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 2b5b32603f334148fede3bc2866367817fd3dcd5ab33aaa40bab84fe3cf49624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208931"
---
# <a name="item-object"></a>Item 物件

Windows影像取得 (WIA) 硬體裝置會表示為 **專案** 物件的階層樹狀結構。 此樹狀結構中的根專案代表裝置本身，而子專案代表影像、資料夾或掃描張床。

使用 **Item** 物件將資料傳輸至檔案、流覽特定裝置的專案樹狀結構，或取得影像或裝置的相關資訊。

## <a name="members"></a>成員

**Item** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Item** 物件具有這些方法。



| 方法                                                         | 描述                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) | **Item** 物件的 [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md)方法會顯示一個對話方塊，可讓使用者選取要從裝置傳送的影像和音訊。<br/>                                                                     |
| [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md)       | **Item** 物件的 [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md)方法會使用 item 屬性的 ID 來傳回其值。<br/>                                                                                                                     |
| [**TakePicture**](-wia-iwiadispatchitem-takepicture.md)       | **Item** 物件的 [**TakePicture**](-wia-iwiadispatchitem-takepicture.md)方法會讓數位相機裝置拍攝圖片，並傳回代表所產生影像的 **專案** 物件。 此方法僅適用于數位相機裝置。<br/> |
| [**傳輸**](-wia-iwiadispatchitem-transfer.md)             | **Item** 物件的 [**Transfer**](-wia-iwiadispatchitem-transfer.md)方法會將資料從裝置傳送到檔案。 此方法僅適用于裝置類型專案。<br/>                                                                                         |



 

### <a name="properties"></a>屬性

**Item** 物件具有這些屬性。



| 屬性                                                                    | 存取類型          | Description                                                                                                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Children**](-wia-iwiadispatchitem-children.md)<br/>               | 唯讀<br/> | **Item** 物件的 [**子**](-wia-iwiadispatchitem-children.md)屬性會抓取 **專案** 物件的集合。 這個集合中的專案代表在階層樹狀結構中，屬於此專案之直接子系的專案。 <br/> |
| [**ConnectStatus**](-wia-iwiadispatchitem-connectstatus.md)<br/>     | 唯讀<br/> | 抓取裝置的連接狀態。 這個屬性只適用于) 的裝置 (根專案類型專案。 如果這個屬性不會套用至專案) ，可能的值為「已連線」、「已中斷連線」或 **Null** (。 <br/>                     |
| [**FirmwareVersion**](-wia-iwiadispatchitem-firmwareversion.md)<br/> | 唯讀<br/> | 捕獲裝置的固件版本。 這個屬性只適用于) 的裝置 (根專案類型專案。 <br/>                                                                                                                                  |
| [**FullName**](-wia-iwiadispatchitem-fullname.md)<br/>               | 唯讀<br/> | 抓取專案顯示在 UI 中的完整名稱。 <br/>                                                                                                                                                                                    |
| [**高度**](-wia-iwiadispatchitem-height.md)<br/>                   | 唯讀<br/> | 專案的高度（以圖元為單位）。 <br/>                                                                                                                                                                                                             |
| [**ItemType**](-wia-iwiadispatchitem-itemtype.md)<br/>               | 唯讀<br/> | 這個專案的型別。 <br/>                                                                                                                                                                                                                          |
| [**Name**](-wia-iwiadispatchitem-name.md)<br/>                       | 唯讀<br/> | 顯示在 UI 中的專案名稱。 <br/>                                                                                                                                                                                                   |
| [**PictureHeight**](-wia-iwiadispatchitem-pictureheight.md)<br/>     | 唯讀<br/> | 此數位相機所產生影像的高度（以圖元為單位）。 僅適用于數位相機。 <br/>                                                                                                                                              |
| [**PictureWidth**](-wia-iwiadispatchitem-picturewidth.md)<br/>       | 唯讀<br/> | 此數位相機所產生影像的寬度（以圖元為單位）。 僅適用于數位相機。 <br/>                                                                                                                                               |
| [**ThumbHeight**](-wia-iwiadispatchitem-thumbheight.md)<br/>         | 唯讀<br/> | 縮圖影像的高度（以圖元為單位）。 如果這個專案不支援縮圖，這個屬性會傳回-1。 <br/>                                                                                                                               |
| [**縮圖**](-wia-iwiadispatchitem-thumbnail.md)<br/>             | 唯讀<br/> | 縮圖影像的路徑和檔案名。 如果專案不支援縮圖，或如果無法建立路徑，則此屬性為 **Null** 。 <br/>                                                                                                  |
| [**ThumbWidth**](-wia-iwiadispatchitem-thumbwidth.md)<br/>           | 唯讀<br/> | 縮圖影像的寬度（以圖元為單位）。 如果這個專案不支援縮圖，這個屬性會傳回-1。 <br/>                                                                                                                                |
| [**時間**](-wia-iwiadispatchitem-time.md)<br/>                       | 唯讀<br/> | 目前的時間。 僅適用于裝置。 <br/>                                                                                                                                                                                                      |
| [**寬度**](-wia-iwiadispatchitem-width.md)<br/>                     | 唯讀<br/> | 專案的寬度（以圖元為單位）。 <br/>                                                                                                                                                                                                              |



 

## <a name="remarks"></a>備註

### <a name="creationaccess-functions"></a>建立 \\ 存取函數

使用下列任何一項來取得物件的參考：



[**TakePicture**](-wia-iwiadispatchitem-takepicture.md)

[**建立**](-wia-iwiadeviceinfo-create.md)

[**建立**](-wia-iwia-create.md)



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




