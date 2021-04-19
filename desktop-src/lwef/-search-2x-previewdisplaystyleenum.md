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
# <a name="previewdisplaystyle-enumeration"></a><span data-ttu-id="e91b4-104">PreviewDisplayStyle 列舉</span><span class="sxs-lookup"><span data-stu-id="e91b4-104">PreviewDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="e91b4-105">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="e91b4-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="e91b4-106">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="e91b4-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="e91b4-107">由 [**IResultsViewer 使用：:P reviewstyle**](-search-2x-iresultsviewer-previewstyle.md) ，以設定或判斷目前正在使用的顯示樣式。</span><span class="sxs-lookup"><span data-stu-id="e91b4-107">Used by [**IResultsViewer::PreviewStyle**](-search-2x-iresultsviewer-previewstyle.md) to set or determine the display style currently being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="e91b4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e91b4-108">Syntax</span></span>


```C++
typedef enum PreviewDisplayStyleEnum { 
  AutoPreview    = 0,
  RightPreview   = 1,
  BottomPreview  = 2,
  NoPreview      = 3
} PreviewDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="e91b4-109">常數</span><span class="sxs-lookup"><span data-stu-id="e91b4-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e91b4-110"><span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**自動**</span><span class="sxs-lookup"><span data-stu-id="e91b4-110"><span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**AutoPreview**</span></span>
</dt> <dd>

<span data-ttu-id="e91b4-111">表示自動預覽。</span><span class="sxs-lookup"><span data-stu-id="e91b4-111">Indicates AutoPreview.</span></span>

</dd> <dt>

<span data-ttu-id="e91b4-112"><span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**RightPreview**</span><span class="sxs-lookup"><span data-stu-id="e91b4-112"><span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**RightPreview**</span></span>
</dt> <dd>

<span data-ttu-id="e91b4-113">表示 RightPreview。</span><span class="sxs-lookup"><span data-stu-id="e91b4-113">Indicates RightPreview.</span></span>

</dd> <dt>

<span data-ttu-id="e91b4-114"><span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**</span><span class="sxs-lookup"><span data-stu-id="e91b4-114"><span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**</span></span>
</dt> <dd>

<span data-ttu-id="e91b4-115">表示 BottomPreview。</span><span class="sxs-lookup"><span data-stu-id="e91b4-115">Indicates BottomPreview.</span></span>

</dd> <dt>

<span data-ttu-id="e91b4-116"><span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**NoPreview**</span><span class="sxs-lookup"><span data-stu-id="e91b4-116"><span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**NoPreview**</span></span>
</dt> <dd>

<span data-ttu-id="e91b4-117">表示 NoPreview。</span><span class="sxs-lookup"><span data-stu-id="e91b4-117">Indicates NoPreview.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e91b4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e91b4-118">Requirements</span></span>



| <span data-ttu-id="e91b4-119">需求</span><span class="sxs-lookup"><span data-stu-id="e91b4-119">Requirement</span></span> | <span data-ttu-id="e91b4-120">值</span><span class="sxs-lookup"><span data-stu-id="e91b4-120">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e91b4-121">Idl</span><span class="sxs-lookup"><span data-stu-id="e91b4-121">IDL</span></span><br/> | <dl> <span data-ttu-id="e91b4-122"><dt>WdsView .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e91b4-122"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





