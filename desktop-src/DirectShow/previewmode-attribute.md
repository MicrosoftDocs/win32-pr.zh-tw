---
description: Previewmode 屬性會指定群組的預覽模式。 如果此值為 TRUE，則框架可能會在預覽期間中斷。 否則，預覽期間不會卸載任何框架。 預設值為 TRUE。
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: previewmode 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3b589b279a11b8ec329641ea2522a6a46dfa0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385695"
---
# <a name="previewmode-attribute"></a>previewmode 屬性

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`previewmode`屬性會指定群組的預覽模式。 如果此值為 **TRUE**，則框架可能會在預覽期間中斷。 否則，預覽期間不會卸載任何框架。 預設值為 **TRUE**。

## <a name="possible-values"></a>可能的值

下列值定義為 TRUE： y、Y、t、T、1。 下列值定義為 FALSE： n、N、f、F、0 (零) 。

## <a name="applies-to"></a>套用至

[**組**](group-element.md)

## <a name="remarks"></a>備註

在預設設定下，預覽緩慢效果或轉換時，會卸載框架，讓影片與音訊保持同步。 這樣的影片看起來可能不穩定。 將此屬性設定為 **FALSE** ，會強制每個框架在預覽期間轉譯，可能導致影片與音訊同步。 寫入檔案時，不會卸載框架。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 屬性](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineGroup::SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 



