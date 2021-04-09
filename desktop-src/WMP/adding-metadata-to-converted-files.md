---
title: 將中繼資料新增至轉換的檔案
description: 將中繼資料新增至轉換的檔案
ms.assetid: 97588651-23de-43ab-b884-76d8af95ab93
keywords:
- Windows Media Player，轉換流程
- Windows Media Player 外掛程式，轉換
- 外掛程式，轉換
- 轉換外掛程式，將中繼資料新增至轉換的檔案
- 將中繼資料新增至轉換的檔案
- 中繼資料，新增至轉換的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4ae47318089149564f64832c95e4cee1b27f26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682466"
---
# <a name="adding-metadata-to-converted-files"></a>將中繼資料新增至轉換的檔案

轉換的檔案必須包含特定的中繼資料，以確保良好的使用者體驗。 轉換後的檔案至少必須包含 [Windows Media 中繼資料使用指導方針](/previous-versions/ms867702(v=msdn.10))中所列的主要屬性。

針對音樂檔案，將 **WM/MediaClassPrimaryID** 的值設定為 D1607DBC-E323-4BE2-86A1-48A42A28441E。

針對語音信箱檔案，將 **WM/MediaClassPrimaryID** 的值設定為01CD0F29-DA4E-4157-897B-6275D50C4F11，也就是音訊檔案的主要類別 GUID。 將 **WM/MediaClassSecondaryID** 的值設定為193c8824-4d52-4178-90bd-305240b04636。

針對語音筆記，將 **WM/MediaClassPrimaryID** 的值設定為01CD0F29-DA4E-4157-897B-6275D50C4F11。 將 **WM/MediaClassSecondaryID** 的值設定為3A172A13-2BD9-4831-835B-114F6A95943F。

將 [ **WM/ContentDistributor** ] 的值設定為提供內容之音樂服務的機碼名稱。

將 [ **WM/UniqueFileIdentifier** ] 的值設定為 [內容識別碼]。 這可讓您在未來取得特定的內容專案。

設定 **WM/WMShadowFileSourceFileType** 的值。

針對受保護的內容，請使用 Windows Media Format SDK 將 **DRM \_ DRMHeader \_ ContentID** 屬性設定為內容識別碼。

針對受保護的內容，請設定 **WM/WMShadowFileSourceDRMType** 的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於轉換外掛程式**](about-conversion-plug-ins.md)
</dt> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 