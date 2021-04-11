---
description: 發生于 InkPicture 控制項的 SizeMode 屬性變更之後。
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: 'InkPicture. SizeModeChanged 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f270ea141bc8803cbcf1ce4e54b0f73318ed69d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320439"
---
# <a name="inkpicturesizemodechanged-event"></a><span data-ttu-id="9ff90-103">InkPicture. SizeModeChanged 事件</span><span class="sxs-lookup"><span data-stu-id="9ff90-103">InkPicture.SizeModeChanged event</span></span>

<span data-ttu-id="9ff90-104">發生于 [InkPicture](inkpicture-control-reference.md)控制項的 [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode)屬性變更之後。</span><span class="sxs-lookup"><span data-stu-id="9ff90-104">Occurs after the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property of the [InkPicture](inkpicture-control-reference.md) control has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff90-105">語法</span><span class="sxs-lookup"><span data-stu-id="9ff90-105">Syntax</span></span>


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a><span data-ttu-id="9ff90-106">參數</span><span class="sxs-lookup"><span data-stu-id="9ff90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ff90-107">*Newmode.obj* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9ff90-107">*NewMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ff90-108">[InkPicture](inkpicture-control-reference.md)控制項的新狀態（以 [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode)屬性的新值為基礎）。</span><span class="sxs-lookup"><span data-stu-id="9ff90-108">The new state of the [InkPicture](inkpicture-control-reference.md) control, based on the new value of the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property.</span></span>

</dd> <dt>

<span data-ttu-id="9ff90-109">*OldMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9ff90-109">*OldMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ff90-110">[InkPicture](inkpicture-control-reference.md)控制項的舊狀態（以 [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode)屬性的舊值為基礎）。</span><span class="sxs-lookup"><span data-stu-id="9ff90-110">The old state of the [InkPicture](inkpicture-control-reference.md) control, based on the old value of the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ff90-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ff90-111">Return value</span></span>

<span data-ttu-id="9ff90-112">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9ff90-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ff90-113">備註</span><span class="sxs-lookup"><span data-stu-id="9ff90-113">Remarks</span></span>

<span data-ttu-id="9ff90-114">此事件方法是在 **\_ IInkPictureEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="9ff90-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="9ff90-115">**\_ IInkPictureEvents** 介面會以 DISPID IPESizeModeChanged 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9ff90-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPESizeModeChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff90-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ff90-116">Requirements</span></span>



| <span data-ttu-id="9ff90-117">需求</span><span class="sxs-lookup"><span data-stu-id="9ff90-117">Requirement</span></span> | <span data-ttu-id="9ff90-118">值</span><span class="sxs-lookup"><span data-stu-id="9ff90-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff90-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ff90-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff90-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ff90-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9ff90-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ff90-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff90-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="9ff90-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9ff90-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9ff90-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ff90-124"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="9ff90-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9ff90-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="9ff90-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="9ff90-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ff90-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9ff90-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ff90-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff90-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="9ff90-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

