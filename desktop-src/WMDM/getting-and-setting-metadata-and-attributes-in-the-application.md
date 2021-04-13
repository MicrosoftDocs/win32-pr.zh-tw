---
title: 存取應用程式中的中繼資料和屬性
description: 取得及設定應用程式中的中繼資料和屬性
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Windows Media 裝置管理員，中繼資料
- 裝置管理員，中繼資料
- 程式設計指南，中繼資料
- 桌面應用程式，中繼資料
- 建立 Windows Media 裝置管理員應用程式，中繼資料
- 中繼資料
- Windows Media 裝置管理員，屬性
- 裝置管理員，屬性
- 程式設計指南，屬性
- 桌面應用程式，屬性
- 建立 Windows Media 裝置管理員應用程式，屬性
- 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a78dbb31ebcc5ec99b1db3503b386b09b5a3c05
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/27/2019
ms.locfileid: "104313851"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a>存取應用程式中的中繼資料和屬性

中繼資料和屬性的一般討論可以 [取得和設定中繼資料和屬性](getting-and-setting-metadata-and-attributes.md)。 本章節涵蓋取得或設定值的特定應用程式方法呼叫。

應用程式可以藉由呼叫 [**IWMDMStorage：： GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)、 [**IWMDMStorage2：： GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2)、 [**IWMDMStorage3：： GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) 或 [**IWMDMStorage4：： GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)，來取得特定儲存體的屬性或中繼資料。 **GetMetadata** 會抓取所有與儲存體相關聯之中繼資料的完整集合，然後應用程式可以列舉所有值或要求集合中的特定值。 **GetSpecifiedMetadata** 會代表呼叫者建立中繼資料物件。 呼叫端可能會藉由在 *ppwszPropNames* 參數中填入所需 Windows Media 裝置管理員屬性字串的陣列，以及該陣列的計數，來要求可用資料的子集。 傳回的中繼資料物件將會填入可抓取的屬性。 無法取出的屬性將不存在。 中繼資料會以最佳方式傳回。

裝置可以藉由呼叫 [**IWMDMStorage：： SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes)、 [**IWMDMStorage2：： SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)或 [**IWMDMStorage3：： >setmetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)來設定儲存體上的屬性或中繼資料。 請注意，不保證任何設定的值都會保存，因為它們可能儲存在非持續性的外部檔案存放區中、可能不支援這些值，或是裝置可能不支援將屬性支援為可寫入。

您也可以藉由呼叫 [**IWMDMDevice3：： GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) 或 [**IWMDMDevice3：： SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty)來取得或設定裝置的相關中繼資料。 [中繼資料常數](metadata-constants.md)的結尾會列出不同的裝置中繼資料常數表格。

每個方法的參考檔中都會提供使用這些方法的範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Windows Media 裝置管理員應用程式**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**取得和設定中繼資料和屬性**](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




