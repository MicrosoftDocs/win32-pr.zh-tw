---
description: 在 InkDivider 物件上設定 LineHeight 屬性。
ms.assetid: ce5e40c5-faa1-4d66-94f4-d5bd1a11ee4c
title: SetLineHeight 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineHeight
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: be4045e01ac890471536d95768668b633d8f2249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996839"
---
# <a name="setlineheight-function"></a><span data-ttu-id="0d907-103">SetLineHeight 函式</span><span class="sxs-lookup"><span data-stu-id="0d907-103">SetLineHeight function</span></span>

<span data-ttu-id="0d907-104">在 [**InkDivider**](inkdivider-class.md)物件上設定 [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)屬性。</span><span class="sxs-lookup"><span data-stu-id="0d907-104">Sets the [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property on the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="0d907-105">此 helper 函式不適合應用程式程式碼使用。</span><span class="sxs-lookup"><span data-stu-id="0d907-105">This helper function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d907-106">語法</span><span class="sxs-lookup"><span data-stu-id="0d907-106">Syntax</span></span>


```C++
HRESULT WINAPI SetLineHeight(
  _In_ INT_PTR hDivider,
  _In_ LONG    lLineHeight
);
```



## <a name="parameters"></a><span data-ttu-id="0d907-107">參數</span><span class="sxs-lookup"><span data-stu-id="0d907-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d907-108">*hDivider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d907-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d907-109">[**InkDivider**](inkdivider-class.md)物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0d907-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="0d907-110">*lLineHeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d907-110">*lLineHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d907-111">[**InkDivider**](inkdivider-class.md)物件的 [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)屬性，以 HIMETRIC 單位表示。</span><span class="sxs-lookup"><span data-stu-id="0d907-111">The [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property of the [**InkDivider**](inkdivider-class.md) object, in HIMETRIC units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d907-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d907-112">Return value</span></span>

<span data-ttu-id="0d907-113">此函數可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0d907-113">This function can return one of these values.</span></span>



| <span data-ttu-id="0d907-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0d907-114">Return code</span></span>                                                                                  | <span data-ttu-id="0d907-115">Description</span><span class="sxs-lookup"><span data-stu-id="0d907-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="0d907-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0d907-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0d907-117">此函數已成功。</span><span class="sxs-lookup"><span data-stu-id="0d907-117">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="0d907-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0d907-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0d907-119">*PDivider* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="0d907-119">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0d907-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d907-120">Requirements</span></span>



| <span data-ttu-id="0d907-121">需求</span><span class="sxs-lookup"><span data-stu-id="0d907-121">Requirement</span></span> | <span data-ttu-id="0d907-122">值</span><span class="sxs-lookup"><span data-stu-id="0d907-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d907-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d907-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0d907-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d907-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="0d907-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d907-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0d907-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="0d907-126">None supported</span></span><br/>                                                             |
| <span data-ttu-id="0d907-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="0d907-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="0d907-128"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d907-128"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 
