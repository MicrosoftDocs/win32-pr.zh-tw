---
description: IWiaUIExtension2：:D eviceDialog 方法-提供可取代預設系統使用者介面的自訂使用者介面。
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: 'IWiaUIExtension2：:D eviceDialog 方法 (Wiadevd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 94e717184c936ae85ba1cf345a13b44f9bbdce4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116646"
---
# <a name="iwiauiextension2devicedialog-method"></a><span data-ttu-id="b34ae-103">IWiaUIExtension2：:D eviceDialog 方法</span><span class="sxs-lookup"><span data-stu-id="b34ae-103">IWiaUIExtension2::DeviceDialog method</span></span>

<span data-ttu-id="b34ae-104">提供可取代預設系統使用者介面的自訂使用者介面。</span><span class="sxs-lookup"><span data-stu-id="b34ae-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b34ae-105">語法</span><span class="sxs-lookup"><span data-stu-id="b34ae-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="b34ae-106">參數</span><span class="sxs-lookup"><span data-stu-id="b34ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b34ae-107">*pDeviceDialogData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b34ae-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b34ae-108">類型： **PDEVICEDIALOGDATA2 \***</span><span class="sxs-lookup"><span data-stu-id="b34ae-108">Type: **PDEVICEDIALOGDATA2\***</span></span>

<span data-ttu-id="b34ae-109">指向 [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) 結構，其中包含執行裝置對話方塊所需的所有資料。</span><span class="sxs-lookup"><span data-stu-id="b34ae-109">Points to a [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b34ae-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b34ae-110">Return value</span></span>

<span data-ttu-id="b34ae-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b34ae-111">Type: **HRESULT**</span></span>

<span data-ttu-id="b34ae-112">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b34ae-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="b34ae-113">如果使用者取消對話方塊，則此方法會傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="b34ae-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="b34ae-114">如果方法失敗，則會傳回適當的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b34ae-114">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="b34ae-115">下表顯示一些可能的傳回狀態碼。</span><span class="sxs-lookup"><span data-stu-id="b34ae-115">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="b34ae-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b34ae-116">Error code</span></span>    | <span data-ttu-id="b34ae-117">描述</span><span class="sxs-lookup"><span data-stu-id="b34ae-117">Description</span></span>                              |
|---------------|------------------------------------------|
| <span data-ttu-id="b34ae-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b34ae-118">E\_INVALIDARG</span></span> | <span data-ttu-id="b34ae-119">參數 pDeviceDialogData 為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b34ae-119">Parameter pDeviceDialogData is **NULL**.</span></span> |
| <span data-ttu-id="b34ae-120">E \_ >NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="b34ae-120">E\_NOTIMPL</span></span>    | <span data-ttu-id="b34ae-121">此方法尚未實作。</span><span class="sxs-lookup"><span data-stu-id="b34ae-121">The method is not implemented.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="b34ae-122">備註</span><span class="sxs-lookup"><span data-stu-id="b34ae-122">Remarks</span></span>

<span data-ttu-id="b34ae-123">如果您執行 [**IWiaUIExtension2**](-wia-iwiauiextension2.md) 介面，但不想取代系統使用者介面，則必須執行此方法，但它應該不會執行任何比傳回 E >notimpl 還多的動作 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b34ae-123">If you implement the [**IWiaUIExtension2**](-wia-iwiauiextension2.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b34ae-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b34ae-124">Requirements</span></span>



| <span data-ttu-id="b34ae-125">需求</span><span class="sxs-lookup"><span data-stu-id="b34ae-125">Requirement</span></span> | <span data-ttu-id="b34ae-126">值</span><span class="sxs-lookup"><span data-stu-id="b34ae-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b34ae-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b34ae-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b34ae-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b34ae-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b34ae-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b34ae-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b34ae-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b34ae-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b34ae-131">標頭</span><span class="sxs-lookup"><span data-stu-id="b34ae-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b34ae-132"><dt>Wiadevd。h</dt></span><span class="sxs-lookup"><span data-stu-id="b34ae-132"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




