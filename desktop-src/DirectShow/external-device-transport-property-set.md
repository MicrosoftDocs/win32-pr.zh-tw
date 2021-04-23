---
description: 外部裝置傳輸屬性集
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: 外部裝置傳輸屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e38217af21ea1839d7c9207a4922bcff00d63a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909216"
---
# <a name="external-device-transport-property-set"></a>外部裝置傳輸屬性集

這個屬性集會控制資料與外部裝置之間的傳輸。 在大部分情況下，應用程式不應該直接使用這個屬性集。 請改用 [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) 介面。

下表列出與使用者模式應用程式相關的屬性。 如需此屬性集的完整說明，請參閱 Microsoft Windows 驅動程式開發工具組 DDK。



| 標籤 | 值 |
|-------------------|---------------------------|
| 屬性集 GUID | PROPSETID \_ EXT \_ TRANSPORT |



 



| 屬性識別碼                                                                           | 描述                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [**KSPROPERTY \_ EXTXPORT \_ ATN \_ 搜尋**](ksproperty-extxport-atn-search.md)           | 搜尋 (ATN) 的絕對曲目編號。 |
| [**KSPROPERTY \_ EXTXPORT 時間 \_ 碼 \_ 搜尋**](ksproperty-extxport-timecode-search.md) | 搜尋時間碼。                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[屬性集](property-sets.md)
</dt> </dl>

 

 



