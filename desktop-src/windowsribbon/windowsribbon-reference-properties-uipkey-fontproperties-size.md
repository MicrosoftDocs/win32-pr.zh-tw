---
title: UI_PKEY_FontProperties_Size
description: 識別 UI \_ PKEY \_ FontProperties \_ Size 屬性。
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae991cfe5f91b4aca4fe0b49a7b7c547e71b0fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968620"
---
# <a name="ui_pkey_fontproperties_size"></a>UI \_ PKEY \_ FontProperties \_ 大小

識別 UI \_ PKEY \_ FontProperties \_ Size 屬性。

```
propertyDescription
   name = UI_PKEY_FontProperties_Size
   shellPKey = UI_PKEY_FontProperties_Size
   formatID = 00000302-7363-696e-8441798acf5aebb7
   propID = 302
   typeInfo
      type = VT_DECIMAL
```

## <a name="remarks"></a>備註

UI \_ PKEY \_ FontProperties \_ 大小是由應用程式用來查詢 **字型大小** 控制項的值。

這個屬性的有效值範圍介於1到9999（含）之間。 如果使用者嘗試輸入不正確值，則會拒絕該專案，而 **字型大小** 控制項會還原為最後一個有效的值。

如果應用程式嘗試以程式設計的方式，將字型大小設為有效範圍以外的值，則功能區架構會使所有字型屬性失效，並將字型控制項 (**字型大小** 和 **字型字型**) 空白或預設狀態（如果適用）。

預設值為 0。

值為0時，會指定不選取任何單一點大小 (任何文字，或是選取 [執行 heterogeneously 大小的文字]) 。

使用者無法將 **字型大小** 控制項設定為0。

除了0以外，UI \_ PKEY \_ FontProperties 大小的有效值 \_ 範圍在 *MinimumFontSize* 和 *MaximumFontSize* 之間的範圍是在 [字型控制項](windowsribbon-controls-fontcontrol.md) 標記中宣告的。

> [!Note]  
> 當字型大小以程式設計方式設定為0時， **字型大小** 控制項會設為空白，例如反白顯示執行 heterogeneously 大小的文字時。

 

選取 [執行 heterogeneously 大小的文字] 時，應用程式應該查詢 [UI \_ PKEY \_ FontProperties \_ DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) 來捕捉 **成長字型** 和 **壓縮字型** 命令。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字型控制項屬性](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[字型控制項](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




