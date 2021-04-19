---
title: PreviewDisplayStyle 列舉
description: 由 IResultsViewer PreviewStyle 用來設定或判斷目前所使用的顯示樣式。
ms.assetid: ccbbfe38-0719-41e0-9331-cc0c1be651eb
keywords:
- PreviewDisplayStyle 列舉舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- PreviewDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11902821ec9fdbbaa9ab8d3fda8971f42fc28c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999710"
---
# <a name="previewdisplaystyle-enumeration"></a>PreviewDisplayStyle 列舉

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。 

由 [**IResultsViewer 使用：:P reviewstyle**](-search-2x-iresultsviewer-previewstyle.md) ，以設定或判斷目前正在使用的顯示樣式。

## <a name="syntax"></a>Syntax


```C++
typedef enum PreviewDisplayStyleEnum { 
  AutoPreview    = 0,
  RightPreview   = 1,
  BottomPreview  = 2,
  NoPreview      = 3
} PreviewDisplayStyle;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**自動**
</dt> <dd>

表示自動預覽。

</dd> <dt>

<span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**RightPreview**
</dt> <dd>

表示 RightPreview。

</dd> <dt>

<span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**
</dt> <dd>

表示 BottomPreview。

</dd> <dt>

<span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**NoPreview**
</dt> <dd>

表示 NoPreview。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>WdsView .idl</dt> </dl> |



 

 





