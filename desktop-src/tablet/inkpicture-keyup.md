---
description: 當 InkPicture 控制項具有焦點時，放開按鍵時發生。
ms.assetid: e22633b5-40fe-4b94-a660-684c4f5c96f3
title: InkPicture (Msinkaut) 的 KeyUp 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2390b6cbb7b91ab8e447df912e591ea37248e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985238"
---
# <a name="inkpicturekeyup-event"></a><span data-ttu-id="4d321-103">InkPicture KeyUp 事件</span><span class="sxs-lookup"><span data-stu-id="4d321-103">InkPicture.KeyUp event</span></span>

<span data-ttu-id="4d321-104">當 [InkPicture](inkpicture-control-reference.md) 控制項具有焦點時，放開按鍵時發生。</span><span class="sxs-lookup"><span data-stu-id="4d321-104">Occurs when a key is released while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d321-105">語法</span><span class="sxs-lookup"><span data-stu-id="4d321-105">Syntax</span></span>


```C++
void KeyUp(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a><span data-ttu-id="4d321-106">參數</span><span class="sxs-lookup"><span data-stu-id="4d321-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d321-107">*KeyCode* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4d321-107">*KeyCode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d321-108">所按下之索引鍵的 ASCII 值。</span><span class="sxs-lookup"><span data-stu-id="4d321-108">The ASCII value of the key that is being pressed.</span></span>

</dd> <dt>

<span data-ttu-id="4d321-109">*Shift* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4d321-109">*Shift* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d321-110">SHIFT 鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="4d321-110">The state of the SHIFT key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d321-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d321-111">Return value</span></span>

<span data-ttu-id="4d321-112">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4d321-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d321-113">備註</span><span class="sxs-lookup"><span data-stu-id="4d321-113">Remarks</span></span>

<span data-ttu-id="4d321-114">此事件方法是在 **\_ IInkPictureEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="4d321-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="4d321-115">**\_ IInkPictureEvents** 介面會以 DISPID IPEKeyUp 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4d321-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d321-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d321-116">Requirements</span></span>



| <span data-ttu-id="4d321-117">需求</span><span class="sxs-lookup"><span data-stu-id="4d321-117">Requirement</span></span> | <span data-ttu-id="4d321-118">值</span><span class="sxs-lookup"><span data-stu-id="4d321-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d321-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d321-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4d321-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d321-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4d321-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d321-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4d321-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="4d321-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4d321-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4d321-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d321-124"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="4d321-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4d321-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="4d321-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d321-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d321-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4d321-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d321-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d321-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="4d321-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

