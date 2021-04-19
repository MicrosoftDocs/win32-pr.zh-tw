---
description: ReadyState 屬性會捕獲 MSWebDVD 物件的 ReadyState。
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: 'ReadyState 屬性 (Ocidl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- READYSTATE
api_type:
- HeaderDef
api_location:
- ocidl.h
ms.openlocfilehash: a52b20349c58e8bd44458266da6a0a33ea149c98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989562"
---
# <a name="readystate-property"></a><span data-ttu-id="cb01a-103">ReadyState 屬性</span><span class="sxs-lookup"><span data-stu-id="cb01a-103">ReadyState Property</span></span>

> [!Note]  
> <span data-ttu-id="cb01a-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="cb01a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="cb01a-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="cb01a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="cb01a-106">`ReadyState`屬性會捕獲 **MSWebDVD** 物件的 ReadyState。</span><span class="sxs-lookup"><span data-stu-id="cb01a-106">The `ReadyState` property retrieves the ReadyState of the **MSWebDVD** object.</span></span>

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a><span data-ttu-id="cb01a-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb01a-107">Return Value</span></span>

<span data-ttu-id="cb01a-108">傳回整數值，代表控制項的 ReadyState。</span><span class="sxs-lookup"><span data-stu-id="cb01a-108">Returns an integer value representing the control's ReadyState.</span></span>



| <span data-ttu-id="cb01a-109">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cb01a-109">Return code</span></span> | <span data-ttu-id="cb01a-110">描述</span><span class="sxs-lookup"><span data-stu-id="cb01a-110">Description</span></span>                                               |
|-------------|-----------------------------------------------------------|
| <span data-ttu-id="cb01a-111">0</span><span class="sxs-lookup"><span data-stu-id="cb01a-111">0</span></span>           | <span data-ttu-id="cb01a-112">預設初始化狀態。</span><span class="sxs-lookup"><span data-stu-id="cb01a-112">Default initialization state.</span></span>                             |
| <span data-ttu-id="cb01a-113">1</span><span class="sxs-lookup"><span data-stu-id="cb01a-113">1</span></span>           | <span data-ttu-id="cb01a-114">物件正在載入其屬性。</span><span class="sxs-lookup"><span data-stu-id="cb01a-114">Object is loading its properties.</span></span>                         |
| <span data-ttu-id="cb01a-115">2</span><span class="sxs-lookup"><span data-stu-id="cb01a-115">2</span></span>           | <span data-ttu-id="cb01a-116">物件已初始化。</span><span class="sxs-lookup"><span data-stu-id="cb01a-116">Object has been initialized.</span></span>                              |
| <span data-ttu-id="cb01a-117">3</span><span class="sxs-lookup"><span data-stu-id="cb01a-117">3</span></span>           | <span data-ttu-id="cb01a-118">物件是互動式的，但並非所有的資料都可供使用。</span><span class="sxs-lookup"><span data-stu-id="cb01a-118">Object is interactive, but not all its data is available.</span></span> |
| <span data-ttu-id="cb01a-119">4</span><span class="sxs-lookup"><span data-stu-id="cb01a-119">4</span></span>           | <span data-ttu-id="cb01a-120">物件已接收其所有資料。</span><span class="sxs-lookup"><span data-stu-id="cb01a-120">Object has received all its data.</span></span>                         |



 

## <a name="remarks"></a><span data-ttu-id="cb01a-121">備註</span><span class="sxs-lookup"><span data-stu-id="cb01a-121">Remarks</span></span>

<span data-ttu-id="cb01a-122">這個屬性是唯讀的，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="cb01a-122">This property is read-only with no default value.</span></span>

<span data-ttu-id="cb01a-123">內嵌在網頁中的任何物件都會公開 `ReadyState` 屬性。</span><span class="sxs-lookup"><span data-stu-id="cb01a-123">Any object embedded in a Web page exposes the `ReadyState` property.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb01a-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb01a-124">Requirements</span></span>



| <span data-ttu-id="cb01a-125">需求</span><span class="sxs-lookup"><span data-stu-id="cb01a-125">Requirement</span></span> | <span data-ttu-id="cb01a-126">值</span><span class="sxs-lookup"><span data-stu-id="cb01a-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cb01a-127">標頭</span><span class="sxs-lookup"><span data-stu-id="cb01a-127">Header</span></span><br/> | <dl> <span data-ttu-id="cb01a-128"><dt>Ocidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb01a-128"><dt>Ocidl.h</dt></span></span> </dl> |



 

 




