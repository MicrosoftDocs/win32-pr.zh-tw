---
title: 'ID 屬性 (TextBox)  (VML) '
description: 'ID 屬性 (TextBox)  (VML) '
ms.assetid: b9eb75cc-4d0a-4e83-a897-e35995ae7c53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b39ac566e7b619c31cb12f4657bd86020dc12cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842448"
---
# <a name="id-attribute-textboxvml"></a><span data-ttu-id="b8eef-103">ID 屬性 (TextBox)  (VML) </span><span class="sxs-lookup"><span data-stu-id="b8eef-103">ID Attribute (TextBox)(VML)</span></span>

<span data-ttu-id="b8eef-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="b8eef-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b8eef-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="b8eef-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b8eef-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="b8eef-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b8eef-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="b8eef-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b8eef-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="b8eef-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b8eef-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="b8eef-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b8eef-110">提供文字方塊唯一識別碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8eef-110">A name that provides a unique identifier for a textbox.</span></span> <span data-ttu-id="b8eef-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b8eef-111">Read/write.</span></span> <span data-ttu-id="b8eef-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="b8eef-112">**String**.</span></span>

<span data-ttu-id="b8eef-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="b8eef-113">**Applies To**</span></span>

[<span data-ttu-id="b8eef-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="b8eef-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="b8eef-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="b8eef-115">**Tag Syntax**</span></span>

<span data-ttu-id="b8eef-116"><v： *element* id = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b8eef-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="b8eef-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="b8eef-117">**Script Syntax**</span></span>

<span data-ttu-id="b8eef-118">*元素* 。 id = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b8eef-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="b8eef-119">*運算式* =*元素*。識別碼</span><span class="sxs-lookup"><span data-stu-id="b8eef-119">*expression*=*element*.id</span></span>

<span data-ttu-id="b8eef-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="b8eef-120">**Remarks**</span></span>

<span data-ttu-id="b8eef-121">使用 **ID** 來參考特定的文字方塊。</span><span class="sxs-lookup"><span data-stu-id="b8eef-121">Use **ID** to refer to a specific textbox.</span></span> <span data-ttu-id="b8eef-122">當您建立 textbox 並指定識別碼之後，您可以在想要操作 textbox 時使用識別碼名稱。</span><span class="sxs-lookup"><span data-stu-id="b8eef-122">Once you have created a textbox and given it an ID, you can use the ID name when you want to manipulate the textbox.</span></span>

<span data-ttu-id="b8eef-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="b8eef-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="b8eef-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="b8eef-124">**Example**</span></span>

<span data-ttu-id="b8eef-125">圖形具有名為 "mytextbox" 的文字方塊識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8eef-125">The shape has a textbox ID called "mytextbox".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 