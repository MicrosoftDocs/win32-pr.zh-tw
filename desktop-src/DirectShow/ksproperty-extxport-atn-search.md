---
description: 此屬性會將命令傳送至裝置，以搜尋 (ATN) 的絕對曲目編號。 UVC 設備磁碟機支援此屬性。
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4115c7ff1c4bc878b4ee80e284f11821c37909a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909445"
---
# <a name="ksproperty_extxport_atn_search"></a>KSPROPERTY \_ EXTXPORT \_ ATN \_ 搜尋

此屬性會將命令傳送至裝置，以搜尋 (ATN) 的絕對曲目編號。 UVC 設備磁碟機支援此屬性。



| 標籤 | 值 |
|-------------------|---------------------------------------|
| 屬性集 GUID | PROPSETID \_ EXT \_ TRANSPORT             |
| 屬性識別碼       | KSPROPERTY \_ EXTXPORT \_ ATN \_ 搜尋     |
| 資料類型         | **KSPROPERTY \_EXTXPORT \_ S** 結構 |



 

## <a name="remarks"></a>備註

將 **KSPROPERTY \_ EXTXPORT \_ S** 結構的 **dwAbsTrackNumber** 成員設定為下列值：


```
(absolute track number << 1) + continuity bit
```



UVC 規格不會定義裝置使用持續性位的方式。 Windows DDK 中說明了 **KSPROPERTY \_ EXTXPORT \_ S** 結構。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[外部裝置傳輸屬性集](external-device-transport-property-set.md)
</dt> </dl>

 

 



