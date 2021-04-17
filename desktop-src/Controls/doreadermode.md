---
title: DoReaderMode 函式
description: 在視窗中啟用讀取器模式。
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- DoReaderMode 函式 Windows 控制項
topic_type:
- apiref
api_name:
- DoReaderMode
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5f5c5863e804cd4bbaab651447e4c6f22dc24a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467128"
---
# <a name="doreadermode-function"></a><span data-ttu-id="77a37-104">DoReaderMode 函式</span><span class="sxs-lookup"><span data-stu-id="77a37-104">DoReaderMode function</span></span>

<span data-ttu-id="77a37-105">\[**DoReaderMode** 可透過 Windows XP Service Pack 2 (SP2) 取得。</span><span class="sxs-lookup"><span data-stu-id="77a37-105">\[**DoReaderMode** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="77a37-106">它可能在後續版本中無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="77a37-106">It may be unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="77a37-107">在視窗中啟用讀取器模式。</span><span class="sxs-lookup"><span data-stu-id="77a37-107">Enables reader mode in a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="77a37-108">語法</span><span class="sxs-lookup"><span data-stu-id="77a37-108">Syntax</span></span>


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a><span data-ttu-id="77a37-109">參數</span><span class="sxs-lookup"><span data-stu-id="77a37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77a37-110">*prmi* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77a37-110">*prmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77a37-111">類型： **PREADERMODEINFO**</span><span class="sxs-lookup"><span data-stu-id="77a37-111">Type: **PREADERMODEINFO**</span></span>

<span data-ttu-id="77a37-112">[**READERMODEINFO**](readermodeinfo.md)結構的指標，其中包含讀取器模式的初始化資訊。</span><span class="sxs-lookup"><span data-stu-id="77a37-112">A pointer to a [**READERMODEINFO**](readermodeinfo.md) structure that contains initialization information for the reader mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77a37-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="77a37-113">Return value</span></span>

<span data-ttu-id="77a37-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="77a37-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="77a37-115">備註</span><span class="sxs-lookup"><span data-stu-id="77a37-115">Remarks</span></span>

<span data-ttu-id="77a37-116">只要按下滑鼠，就可以透過支援的裝置來啟用讀者模式，通常是使用第三個滑鼠按鍵或滾輪。</span><span class="sxs-lookup"><span data-stu-id="77a37-116">Reader mode is activated through supported devices by a mouse click, typically using a third mouse button or scroll wheel.</span></span> <span data-ttu-id="77a37-117">在指定區域中的後續滑鼠移動會滾動該區域的內容，而不是移動指標。</span><span class="sxs-lookup"><span data-stu-id="77a37-117">Subsequent mouse movement in a specified area scrolls that area's contents rather than moving a pointer.</span></span> <span data-ttu-id="77a37-118">在該區域外，滑鼠指標會顯示並正常運作。</span><span class="sxs-lookup"><span data-stu-id="77a37-118">Outside of that area, the mouse pointer is displayed and operates normally.</span></span> <span data-ttu-id="77a37-119">第二次按一下按鈕或滾輪會從讀取器模式釋放裝置。</span><span class="sxs-lookup"><span data-stu-id="77a37-119">A second click of the button or scroll wheel releases the device from reader mode.</span></span>

> [!Note]  
> <span data-ttu-id="77a37-120">未在任何公用標頭中宣告此函式。</span><span class="sxs-lookup"><span data-stu-id="77a37-120">This function is not declared in any public header.</span></span> <span data-ttu-id="77a37-121">若要使用它，您必須以 Comctl32.dll 的序數383形式存取它。</span><span class="sxs-lookup"><span data-stu-id="77a37-121">To use it, you must access it as ordinal 383 from Comctl32.dll.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="77a37-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="77a37-122">Requirements</span></span>



| <span data-ttu-id="77a37-123">需求</span><span class="sxs-lookup"><span data-stu-id="77a37-123">Requirement</span></span> | <span data-ttu-id="77a37-124">值</span><span class="sxs-lookup"><span data-stu-id="77a37-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77a37-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77a37-125">Minimum supported client</span></span><br/> | <span data-ttu-id="77a37-126">Windows Vista、Windows Vista \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77a37-126">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="77a37-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77a37-127">Minimum supported server</span></span><br/> | <span data-ttu-id="77a37-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77a37-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="77a37-129">DLL</span><span class="sxs-lookup"><span data-stu-id="77a37-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77a37-130"><dt>Comctl32.dll (4.72 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="77a37-130"><dt>Comctl32.dll (version 4.72 or later)</dt></span></span> </dl> |



 

 





