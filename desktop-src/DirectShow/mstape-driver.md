---
description: MSTape 驅動程式
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: MSTape 驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f37e22c26866fca9519219d358e9733fb56151
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845755"
---
# <a name="mstape-driver"></a>MSTape 驅動程式

本主題適用于 Windows XP 或更新版本。

MSTape 驅動程式支援 D-VHS 和 MPEG 攝像機裝置。 它會以 [WDM 影片捕獲](wdm-video-capture-filter.md) 篩選器的形式公開給應用程式。 它的功能與 [MSDV](msdv-driver.md)的 DV 攝像機驅動程式類似：

-   它會出現在「影片捕獲來源」 (CLSID \_ VideoInputDeviceCategory) 和「WDM 串流轉譯裝置」 (AM \_ KSCATEGORY 轉譯 \_) 篩選分類。
-   應用程式可以使用 [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) 介面來建立篩選準則的實例。
-   它具有用來從裝置進行捕捉和傳輸的輸出 pin，以及用於傳輸至裝置的輸入 pin。 一次只能連接一個 pin。

**媒體類型**

輸入 pin 支援一種媒體類型。



|              |                                                            |
|--------------|------------------------------------------------------------|
| 主要類型   | 媒體媒體的 \_ 串流                                          |
| Subtype      | MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ STRIDE                     |
| 取樣大小  | 192 x 256                                                  |
| 格式區塊 | [**MPEG2 \_ 傳輸 \_ STRIDE**](mpeg2-transport-stride.md) |



 

輸出 pin 支援兩種媒體類型。



|              |                                        |
|--------------|----------------------------------------|
| 主要類型   | 媒體媒體的 \_ 串流                      |
| Subtype      | MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ STRIDE |
| 取樣大小  | 192 x 256                              |
| 格式區塊 | MPEG2 \_ 傳輸 \_ STRIDE               |



 



|              |                                        |
|--------------|----------------------------------------|
| 主要類型   | 媒體媒體的 \_ 串流                      |
| Subtype      | MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ STRIDE |
| 取樣大小  | 188 x 256                              |
| 格式區塊 | **NULL**                               |



 

**裝置資訊**

驅動程式會動態讀取裝置設定 ROM 的資訊。 應用程式可以藉由將裝置的標記系結至屬性包，並呼叫 **IPropertyBag：： Read** 方法，來取得這項資訊。



| 屬性            | 描述                                                                                                                                                                         | 資料類型           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| UniqueID \_ 低       | 裝置 (低 **DWORD**) 的唯一識別碼。                                                                                                                                            | **long** (VT \_ I4)    |
| UniqueID \_ 高      | 裝置 (高 **DWORD**) 的唯一識別碼                                                                                                                                            | **long**            |
| VendorID            | 廠商識別碼。                                                                                                                                                                          | **long**            |
| ModelID             | 模型識別碼。                                                                                                                                                                           | **long**            |
| VendorText          | 廠商名稱。                                                                                                                                                                        | **BSTR** (VT \_ bstr)  |
| ModelText           | 裝置型號名稱。                                                                                                                                                                  | **BSTR**            |
| UnitModelText       | 單位模型名稱;可能與 ModelText 相同。                                                                                                                                      | **BSTR**            |
| DeviceOPcr0Payload  | oPCR (輸出外掛程式控制項) 承載。 範例： 146 quadlets。                                                                                                                          | **long**            |
| DeviceOPcr0DataRate | oPCR 資料速率。 範例： 0 (S100) 、1 (S200) 或 2 (S400) 。                                                                                                                          | **long**            |
| DeviceClassGUID     | 識別設備磁碟機的 GUID。 若為 MSTape，此值為 `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` 。 此 GUID 在標頭檔 Xprtdefs 中定義為 MSTapeDeviceGUID。 | **BSTR**            |
| Description         | 從 INF 檔案取得之裝置的描述。 此字串通常包含裝置的品牌名稱。                                                                    | **BSTR**            |



 

裝置識別碼是64位的整數。 低 **dword** 會儲存在 uniqueid \_ low 屬性中，而高 **Dword** 會儲存在 uniqueid \_ high 屬性中。

如需裝置名字標記的詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[控制 DV 攝像機](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



