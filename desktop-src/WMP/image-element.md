---
title: " (WMP SDK) 的 Image 元素"
description: 請注意，本節將說明針對線上商店使用而設計的功能。 | (WMP SDK) 的 Image 元素
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- 影像元素 Windows Media Player
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c10b62365453f395c1aaf373e355c21260900f8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976180"
---
# <a name="image-element-wmp-sdk"></a> (WMP SDK) 的 Image 元素

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**Image** 元素會指定 Windows Media Player 顯示給使用者以代表線上商店的影像。

``` syntax
<Image
    EulaURL = "URL"
    MenuURL = "URL"
    ServiceLargeURL = "URL"
    ServiceSmallURL = "URL"
/>
```

## <a name="attributes"></a>屬性

<dl> <dt>

<span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>類型1存放區所需的 **EulaURL** (，已忽略類型 2) 
</dt> <dd>

Windows Media Player 在 [使用者授權合約] ([EULA) ] 對話方塊中顯示之標誌的 URL。 這必須是 80 x 80 圖元的 PNG 影像。

</dd> <dt>

<span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (選用) 
</dt> <dd>

Windows Media Player 在 [服務] 功能表上顯示之影像的 URL。 此映射必須是 15 x 15 圖元。

</dd> <dt>

<span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (選用) 
</dt> <dd>

針對類型1線上商店，這是 Windows Media Player 在 [ **線上商店** ] 索引標籤中顯示之影像的 URL。針對 Windows Media Player 11，此映射的寬度必須為45圖元，且高度為13圖元。 針對 Windows Media Player 12，此映射的寬度必須為45圖元，高達30圖元。 若要支援 Windows Media Player 的11和12版，您必須提供兩個不同的 ServiceInfo.xml 檔，其中每個檔都指向適當大小的 ServiceLargeURL 影像。

針對第2類型的線上商店，這是 Windows Media Player 顯示在 [ **線上商店** ] 索引標籤旁邊或 [工作窗格] 按鈕旁邊之影像的 URL。 此映射必須是 30 x 30 圖元。

</dd> <dt>

<span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (選用) 
</dt> <dd>

顯示的標誌 URL，以及 **description** 元素中指定的行銷描述。 如果未提供，則會是空白。  (所有類型，選擇性) 這必須是45圖元寬和13圖元高的 PNG 影像。

</dd> </dl>

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素         |
|-----------------|-----------------|
| 父元素 | **ServiceInfo** |
| 子元素  | 無            |



 

## <a name="remarks"></a>備註

支援的影像格式為 .gif、.jpg、.bmp 和 .png (這是建議的格式) 。 支援和建議使用 Web 透明度。 不支援動畫 GIF 檔。

如果您未提供 **MenuURL** 的值，Windows Media Player 在線上商店的功能表上，不會顯示任何圖形。

您可以提供 ServiceLargeURL 的動畫影像。 在 Windows Media Player 10 或11中，影像會以動畫顯示。 在 Windows Media Player 12 中，只會顯示影像的第一個畫面格。 若要提供動畫影像，請建立包含動畫後續畫面格的單一影像檔案。 例如，對於30圖元寬和30圖元高的影像，您可以在600圖元寬和30圖元高的影像中並排提供20個後續影像。 Windows Media Player 會自動將20個個別影像顯示在另一個影像上，以建立這類影像的動畫。 此動畫只會在線上商店開啟時出現一次;它不會重複。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Type 2 線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

 





