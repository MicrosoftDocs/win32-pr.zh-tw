---
description: 表示著色器偵錯工具要求的相關資訊。
MS-HAID: vspixengine.DebugShaderRequestInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DebugShaderRequestInfo 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DEFFAEE4-6C53-4C89-A533-A5BE73B80DEA
api_name:
- DebugShaderRequestInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a59bfb84bb7d4e8644c0cfadc4475be7d7da4a54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510058"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span data-ttu-id="dc59c-103"><span id="vspixengine.debugshaderrequestinfo"></span>DebugShaderRequestInfo 結構</span><span class="sxs-lookup"><span data-stu-id="dc59c-103"><span id="vspixengine.debugshaderrequestinfo"></span>DebugShaderRequestInfo structure</span></span>

<span data-ttu-id="dc59c-104">表示著色器偵錯工具要求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dc59c-104">Represents information about a shader debugger request.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc59c-105">語法</span><span class="sxs-lookup"><span data-stu-id="dc59c-105">Syntax</span></span>


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a><span data-ttu-id="dc59c-106">成員</span><span class="sxs-lookup"><span data-stu-id="dc59c-106">Members</span></span>

<span data-ttu-id="dc59c-107">**階段**</span><span class="sxs-lookup"><span data-stu-id="dc59c-107">**stage**</span></span>  
<span data-ttu-id="dc59c-108">要進行調試的管線階段。</span><span class="sxs-lookup"><span data-stu-id="dc59c-108">The pipeline stage to debug.</span></span>

<span data-ttu-id="dc59c-109">**eventID**</span><span class="sxs-lookup"><span data-stu-id="dc59c-109">**eventID**</span></span>  
<span data-ttu-id="dc59c-110">要進行偵錯工具之圖形事件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc59c-110">The ID of the graphics event to debug.</span></span>

<span data-ttu-id="dc59c-111">**frameNumber**</span><span class="sxs-lookup"><span data-stu-id="dc59c-111">**frameNumber**</span></span>  
<span data-ttu-id="dc59c-112">要進行調試的框架。</span><span class="sxs-lookup"><span data-stu-id="dc59c-112">The frame to debug.</span></span>

<span data-ttu-id="dc59c-113">**頂點**</span><span class="sxs-lookup"><span data-stu-id="dc59c-113">**vertex**</span></span>  
<span data-ttu-id="dc59c-114">要調試的頂點。</span><span class="sxs-lookup"><span data-stu-id="dc59c-114">The vertex to debug.</span></span>

<span data-ttu-id="dc59c-115">**像素**</span><span class="sxs-lookup"><span data-stu-id="dc59c-115">**pixel**</span></span>  
<span data-ttu-id="dc59c-116">要調試的圖元。</span><span class="sxs-lookup"><span data-stu-id="dc59c-116">The pixel to debug.</span></span>

<span data-ttu-id="dc59c-117">**groupCoordinates**</span><span class="sxs-lookup"><span data-stu-id="dc59c-117">**groupCoordinates**</span></span>  
<span data-ttu-id="dc59c-118">要進行偵錯工具之群組的座標。</span><span class="sxs-lookup"><span data-stu-id="dc59c-118">The coordinates of the group to debug.</span></span>

<span data-ttu-id="dc59c-119">**threadCoordinates**</span><span class="sxs-lookup"><span data-stu-id="dc59c-119">**threadCoordinates**</span></span>  
<span data-ttu-id="dc59c-120">要進行偵錯工具之執行緒的座標</span><span class="sxs-lookup"><span data-stu-id="dc59c-120">The coordinates of the thread to debug</span></span>

## <a name="requirements"></a><span data-ttu-id="dc59c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc59c-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="dc59c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="dc59c-122">Header</span></span></p></td><td><span data-ttu-id="dc59c-123">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="dc59c-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



