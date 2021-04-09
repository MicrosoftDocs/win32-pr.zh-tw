---
description: 刪除 InkDivider 物件，並釋放相關聯的資源。
ms.assetid: adf772e0-2829-4410-83c4-45a24bf3a848
title: DeleteInkDivider 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteInkDivider
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 8338d179b0bd57232463c794feca96885ee006fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851619"
---
# <a name="deleteinkdivider-function"></a><span data-ttu-id="edb43-103">DeleteInkDivider 函式</span><span class="sxs-lookup"><span data-stu-id="edb43-103">DeleteInkDivider function</span></span>

<span data-ttu-id="edb43-104">刪除 [**InkDivider**](inkdivider-class.md) 物件，並釋放相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="edb43-104">Deletes an [**InkDivider**](inkdivider-class.md) object and releases associated resources.</span></span>

<span data-ttu-id="edb43-105">此函式不適合應用程式程式碼使用。</span><span class="sxs-lookup"><span data-stu-id="edb43-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb43-106">語法</span><span class="sxs-lookup"><span data-stu-id="edb43-106">Syntax</span></span>


```C++
HRESULT WINAPI DeleteInkDivider(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a><span data-ttu-id="edb43-107">參數</span><span class="sxs-lookup"><span data-stu-id="edb43-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb43-108">*hDivider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="edb43-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb43-109">[**InkDivider**](inkdivider-class.md)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="edb43-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edb43-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="edb43-110">Return value</span></span>

<span data-ttu-id="edb43-111">此函數可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="edb43-111">This function can return one of these values.</span></span>



| <span data-ttu-id="edb43-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="edb43-112">Return code</span></span>                                                                                  | <span data-ttu-id="edb43-113">Description</span><span class="sxs-lookup"><span data-stu-id="edb43-113">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="edb43-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="edb43-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="edb43-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="edb43-115">The method succeeded.</span></span><br/>                |
| <dl> <span data-ttu-id="edb43-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="edb43-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="edb43-117">*HDivider* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="edb43-117">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="edb43-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="edb43-118">Requirements</span></span>



| <span data-ttu-id="edb43-119">需求</span><span class="sxs-lookup"><span data-stu-id="edb43-119">Requirement</span></span> | <span data-ttu-id="edb43-120">值</span><span class="sxs-lookup"><span data-stu-id="edb43-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edb43-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="edb43-121">Minimum supported client</span></span><br/> | <span data-ttu-id="edb43-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="edb43-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="edb43-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="edb43-123">Minimum supported server</span></span><br/> | <span data-ttu-id="edb43-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="edb43-124">None supported</span></span><br/>                                                             |
| <span data-ttu-id="edb43-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="edb43-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="edb43-126"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edb43-126"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




