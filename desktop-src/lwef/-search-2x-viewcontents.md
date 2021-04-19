---
title: ViewContents 列舉
description: 由 IResultsViewer 內容用來指出或設定目前查詢傳回集的顯示方式。
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- ViewContents 列舉舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- ViewContents
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f465b16ef81dd71695f8de0b04b6d7567480f4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995517"
---
# <a name="viewcontents-enumeration"></a><span data-ttu-id="17835-104">ViewContents 列舉</span><span class="sxs-lookup"><span data-stu-id="17835-104">ViewContents enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="17835-105">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="17835-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="17835-106">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="17835-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="17835-107">由 [**IResultsViewer：：內容**](-search-2x-iresultsviewer-contents.md) 用來指出或設定目前查詢傳回集的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="17835-107">Used by [**IResultsViewer::Contents**](-search-2x-iresultsviewer-contents.md) to indicate or set how the current query return set is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="17835-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="17835-108">Syntax</span></span>


```C++
typedef enum ViewContentsEnum { 
  ResultsDisplayed     = 0,
  ShellViewDisplayed   = 1,
  WebBrowserDisplayed  = 2
} ViewContents;
```



## <a name="constants"></a><span data-ttu-id="17835-109">常數</span><span class="sxs-lookup"><span data-stu-id="17835-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="17835-110"><span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**</span><span class="sxs-lookup"><span data-stu-id="17835-110"><span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="17835-111">指出顯示在結果檢視中的內容類型。</span><span class="sxs-lookup"><span data-stu-id="17835-111">Indicates the type of contents being displayed in the results view.</span></span>

</dd> <dt>

<span data-ttu-id="17835-112"><span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**</span><span class="sxs-lookup"><span data-stu-id="17835-112"><span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="17835-113">表示顯示在結果檢視中的內容類型目前設定為 Shell 視圖。</span><span class="sxs-lookup"><span data-stu-id="17835-113">Indicates the type of contents being displayed in the results view is currently set to the Shell view.</span></span>

</dd> <dt>

<span data-ttu-id="17835-114"><span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**</span><span class="sxs-lookup"><span data-stu-id="17835-114"><span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="17835-115">表示顯示在結果檢視中的內容類型目前設定為瀏覽器視圖。</span><span class="sxs-lookup"><span data-stu-id="17835-115">Indicates the type of contents being displayed in the results view is currently set to the browser view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17835-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="17835-116">Requirements</span></span>



| <span data-ttu-id="17835-117">需求</span><span class="sxs-lookup"><span data-stu-id="17835-117">Requirement</span></span> | <span data-ttu-id="17835-118">值</span><span class="sxs-lookup"><span data-stu-id="17835-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17835-119">Idl</span><span class="sxs-lookup"><span data-stu-id="17835-119">IDL</span></span><br/> | <dl> <span data-ttu-id="17835-120"><dt>WdsView .idl</dt></span><span class="sxs-lookup"><span data-stu-id="17835-120"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





