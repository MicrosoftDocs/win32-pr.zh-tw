---
description: IWiaUIExtension：:D eviceDialog 方法-提供可取代預設系統使用者介面的自訂使用者介面。
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: 'IWiaUIExtension：:D eviceDialog 方法 (Wiadevd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: d467769308707032b8e92b4ac7877488991356dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116706"
---
# <a name="iwiauiextensiondevicedialog-method"></a><span data-ttu-id="24f5a-103">IWiaUIExtension：:D eviceDialog 方法</span><span class="sxs-lookup"><span data-stu-id="24f5a-103">IWiaUIExtension::DeviceDialog method</span></span>

<span data-ttu-id="24f5a-104">提供可取代預設系統使用者介面的自訂使用者介面。</span><span class="sxs-lookup"><span data-stu-id="24f5a-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="24f5a-105">語法</span><span class="sxs-lookup"><span data-stu-id="24f5a-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="24f5a-106">參數</span><span class="sxs-lookup"><span data-stu-id="24f5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24f5a-107">*pDeviceDialogData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24f5a-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f5a-108">類型： **PDEVICEDIALOGDATA \***</span><span class="sxs-lookup"><span data-stu-id="24f5a-108">Type: **PDEVICEDIALOGDATA\***</span></span>

<span data-ttu-id="24f5a-109">指向 [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) 結構，其中包含執行裝置對話方塊所需的所有資料。</span><span class="sxs-lookup"><span data-stu-id="24f5a-109">Points to a [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24f5a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="24f5a-110">Return value</span></span>

<span data-ttu-id="24f5a-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="24f5a-111">Type: **HRESULT**</span></span>

<span data-ttu-id="24f5a-112">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="24f5a-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="24f5a-113">如果使用者取消對話方塊，則此方法會傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="24f5a-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="24f5a-114">如果未執行此方法，則會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="24f5a-114">If the method is not implemented, it returns E\_NOTIMPL.</span></span> <span data-ttu-id="24f5a-115">如果方法失敗，則會傳回標準 COM 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="24f5a-115">If the method fails, it returns a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="24f5a-116">備註</span><span class="sxs-lookup"><span data-stu-id="24f5a-116">Remarks</span></span>

<span data-ttu-id="24f5a-117">如果您執行 [**IWiaUIExtension**](-wia-iwiauiextension.md) 介面，但不想取代系統使用者介面，則必須執行此方法，但它應該不會執行任何比傳回 E >notimpl 還多的動作 \_ 。</span><span class="sxs-lookup"><span data-stu-id="24f5a-117">If you implement the [**IWiaUIExtension**](-wia-iwiauiextension.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="24f5a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="24f5a-118">Requirements</span></span>



| <span data-ttu-id="24f5a-119">需求</span><span class="sxs-lookup"><span data-stu-id="24f5a-119">Requirement</span></span> | <span data-ttu-id="24f5a-120">值</span><span class="sxs-lookup"><span data-stu-id="24f5a-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="24f5a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24f5a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="24f5a-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24f5a-122">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="24f5a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24f5a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="24f5a-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24f5a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="24f5a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="24f5a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="24f5a-126"><dt>Wiadevd。h</dt></span><span class="sxs-lookup"><span data-stu-id="24f5a-126"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




