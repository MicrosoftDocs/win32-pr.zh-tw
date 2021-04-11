---
description: 測試 InkDivider 物件是否可以使用 InkRecognizerCoNtext 類別來分析文字。
ms.assetid: fd848fcc-5258-401f-8b51-b9d57da173da
title: RecognizerCoNtextSet 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizerContextSet
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 51e75b810c2103afed2e8ac8a28706b9c9af5da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849696"
---
# <a name="recognizercontextset-function"></a><span data-ttu-id="ed5bf-103">RecognizerCoNtextSet 函式</span><span class="sxs-lookup"><span data-stu-id="ed5bf-103">RecognizerContextSet function</span></span>

<span data-ttu-id="ed5bf-104">測試 [**InkDivider**](inkdivider-class.md) 物件是否可以使用 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 類別來分析文字。</span><span class="sxs-lookup"><span data-stu-id="ed5bf-104">Tests whether the [**InkDivider**](inkdivider-class.md) object can use the [**InkRecognizerContext**](inkrecognizercontext-class.md) class to analyze words.</span></span>

<span data-ttu-id="ed5bf-105">此函式不適合應用程式程式碼使用。</span><span class="sxs-lookup"><span data-stu-id="ed5bf-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed5bf-106">語法</span><span class="sxs-lookup"><span data-stu-id="ed5bf-106">Syntax</span></span>


```C++
HRESULT WINAPI RecognizerContextSet(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a><span data-ttu-id="ed5bf-107">參數</span><span class="sxs-lookup"><span data-stu-id="ed5bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed5bf-108">*hDivider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ed5bf-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed5bf-109">[**InkDivider**](inkdivider-class.md)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ed5bf-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed5bf-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed5bf-110">Return value</span></span>

<span data-ttu-id="ed5bf-111">此函數可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ed5bf-111">This function can return one of these values.</span></span>



| <span data-ttu-id="ed5bf-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ed5bf-112">Return code</span></span>                                                                                  | <span data-ttu-id="ed5bf-113">Description</span><span class="sxs-lookup"><span data-stu-id="ed5bf-113">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="ed5bf-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ed5bf-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ed5bf-115">此函數已成功。</span><span class="sxs-lookup"><span data-stu-id="ed5bf-115">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="ed5bf-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ed5bf-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ed5bf-117">*PDivider* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="ed5bf-117">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ed5bf-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed5bf-118">Requirements</span></span>



| <span data-ttu-id="ed5bf-119">需求</span><span class="sxs-lookup"><span data-stu-id="ed5bf-119">Requirement</span></span> | <span data-ttu-id="ed5bf-120">值</span><span class="sxs-lookup"><span data-stu-id="ed5bf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed5bf-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed5bf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ed5bf-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed5bf-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ed5bf-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed5bf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ed5bf-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="ed5bf-124">None supported</span></span><br/>                                                             |
| <span data-ttu-id="ed5bf-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="ed5bf-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="ed5bf-126"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed5bf-126"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




