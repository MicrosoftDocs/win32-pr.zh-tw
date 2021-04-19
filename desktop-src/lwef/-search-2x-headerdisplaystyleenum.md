---
title: HeaderDisplayStyle 列舉
description: 由 IResultsViewer HeaderStyle 用來設定或傳回目前的標頭樣式。
ms.assetid: 13ae6317-d990-4ccf-83b3-275caf953611
keywords:
- HeaderDisplayStyle 列舉舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- HeaderDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc65b17fa61b799fc9ab8ea7cc1b01380a5843c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994077"
---
# <a name="headerdisplaystyle-enumeration"></a><span data-ttu-id="e42ef-104">HeaderDisplayStyle 列舉</span><span class="sxs-lookup"><span data-stu-id="e42ef-104">HeaderDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="e42ef-105">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="e42ef-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="e42ef-106">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="e42ef-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="e42ef-107">由 [**IResultsViewer：： HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) 用來設定或傳回目前的標頭樣式。</span><span class="sxs-lookup"><span data-stu-id="e42ef-107">Used by [**IResultsViewer::HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) to set or return the current header style.</span></span>

## <a name="syntax"></a><span data-ttu-id="e42ef-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e42ef-108">Syntax</span></span>


```C++
typedef enum HeaderDisplayStyleEnum { 
  FullHeader     = 0,
  CompactHeader  = 1,
  NoHeader       = 2
} HeaderDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="e42ef-109">常數</span><span class="sxs-lookup"><span data-stu-id="e42ef-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e42ef-110"><span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**</span><span class="sxs-lookup"><span data-stu-id="e42ef-110"><span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**</span></span>
</dt> <dd>

<span data-ttu-id="e42ef-111">指出或設定完整標頭的使用。</span><span class="sxs-lookup"><span data-stu-id="e42ef-111">Indicates or sets the use of full headers.</span></span>

</dd> <dt>

<span data-ttu-id="e42ef-112"><span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**</span><span class="sxs-lookup"><span data-stu-id="e42ef-112"><span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**</span></span>
</dt> <dd>

<span data-ttu-id="e42ef-113">指出或設定壓縮標頭的使用。</span><span class="sxs-lookup"><span data-stu-id="e42ef-113">Indicates or sets the use of compact headers.</span></span>

</dd> <dt>

<span data-ttu-id="e42ef-114"><span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**NoHeader**</span><span class="sxs-lookup"><span data-stu-id="e42ef-114"><span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**NoHeader**</span></span>
</dt> <dd>

<span data-ttu-id="e42ef-115">表示或設定不使用標頭。</span><span class="sxs-lookup"><span data-stu-id="e42ef-115">Indicates or sets the use of no headers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e42ef-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e42ef-116">Requirements</span></span>



| <span data-ttu-id="e42ef-117">需求</span><span class="sxs-lookup"><span data-stu-id="e42ef-117">Requirement</span></span> | <span data-ttu-id="e42ef-118">值</span><span class="sxs-lookup"><span data-stu-id="e42ef-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e42ef-119">Idl</span><span class="sxs-lookup"><span data-stu-id="e42ef-119">IDL</span></span><br/> | <dl> <span data-ttu-id="e42ef-120"><dt>WdsView .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e42ef-120"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





