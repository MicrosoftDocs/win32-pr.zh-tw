---
description: 發生于 InkPicture 控制項具有焦點時按下按鍵時。
ms.assetid: adb61eff-a92c-40b0-940c-02e14cd34e5f
title: 'InkPicture： KeyPress 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f9ef48a0e117d6a3d4c29a9ca69aba3bf6e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943540"
---
# <a name="inkpicturekeypress-event"></a><span data-ttu-id="c6d04-103">InkPicture 的按鍵事件</span><span class="sxs-lookup"><span data-stu-id="c6d04-103">InkPicture.KeyPress event</span></span>

<span data-ttu-id="c6d04-104">發生于 [InkPicture](inkpicture-control-reference.md) 控制項具有焦點時按下按鍵時。</span><span class="sxs-lookup"><span data-stu-id="c6d04-104">Occurs when a key is pressed while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6d04-105">語法</span><span class="sxs-lookup"><span data-stu-id="c6d04-105">Syntax</span></span>


```C++
void KeyPress(
  [in, out] short *KeyAscii
);
```



## <a name="parameters"></a><span data-ttu-id="c6d04-106">參數</span><span class="sxs-lookup"><span data-stu-id="c6d04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6d04-107">*KeyAscii* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c6d04-107">*KeyAscii* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6d04-108">所按下之索引鍵的 ASCII 值。</span><span class="sxs-lookup"><span data-stu-id="c6d04-108">The ASCII value of the key that is being pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6d04-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6d04-109">Return value</span></span>

<span data-ttu-id="c6d04-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c6d04-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6d04-111">備註</span><span class="sxs-lookup"><span data-stu-id="c6d04-111">Remarks</span></span>

<span data-ttu-id="c6d04-112">此事件方法是在 **\_ IInkPictureEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="c6d04-112">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="c6d04-113">**\_ IInkPictureEvents** 介面會以 DISPID IPEKeyPress 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c6d04-113">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyPress.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6d04-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6d04-114">Requirements</span></span>



| <span data-ttu-id="c6d04-115">需求</span><span class="sxs-lookup"><span data-stu-id="c6d04-115">Requirement</span></span> | <span data-ttu-id="c6d04-116">值</span><span class="sxs-lookup"><span data-stu-id="c6d04-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d04-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6d04-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c6d04-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6d04-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c6d04-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6d04-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c6d04-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="c6d04-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c6d04-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c6d04-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6d04-122"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c6d04-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c6d04-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="c6d04-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6d04-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6d04-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c6d04-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6d04-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d04-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="c6d04-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

