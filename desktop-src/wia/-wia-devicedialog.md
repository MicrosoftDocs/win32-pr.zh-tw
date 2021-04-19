---
description: 由應用程式用來向使用者顯示裝置對話方塊。
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: 'DeviceDialog 函式 (Wiadevd) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceDialog
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7389b0466dadf530da6fb7cd386d8a57d92cf1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982438"
---
# <a name="devicedialog-function"></a><span data-ttu-id="8787b-103">DeviceDialog 函式</span><span class="sxs-lookup"><span data-stu-id="8787b-103">DeviceDialog function</span></span>

<span data-ttu-id="8787b-104">由應用程式用來向使用者顯示裝置對話方塊。</span><span class="sxs-lookup"><span data-stu-id="8787b-104">Used by applications to display a device dialog box to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="8787b-105">語法</span><span class="sxs-lookup"><span data-stu-id="8787b-105">Syntax</span></span>


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="8787b-106">參數</span><span class="sxs-lookup"><span data-stu-id="8787b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8787b-107">*pDeviceDialogData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8787b-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8787b-108">類型： **PDEVICEDIALOGDATA**</span><span class="sxs-lookup"><span data-stu-id="8787b-108">Type: **PDEVICEDIALOGDATA**</span></span>

<span data-ttu-id="8787b-109">用來建立裝置對話方塊的 [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) 。</span><span class="sxs-lookup"><span data-stu-id="8787b-109">The [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) to use to create the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8787b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="8787b-110">Return value</span></span>

<span data-ttu-id="8787b-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8787b-111">Type: **HRESULT**</span></span>

<span data-ttu-id="8787b-112">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="8787b-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8787b-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8787b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8787b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8787b-114">Requirements</span></span>



| <span data-ttu-id="8787b-115">需求</span><span class="sxs-lookup"><span data-stu-id="8787b-115">Requirement</span></span> | <span data-ttu-id="8787b-116">值</span><span class="sxs-lookup"><span data-stu-id="8787b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8787b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8787b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8787b-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8787b-118">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8787b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8787b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8787b-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8787b-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8787b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="8787b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8787b-122"><dt>Wiadevd。h</dt></span><span class="sxs-lookup"><span data-stu-id="8787b-122"><dt>Wiadevd.h</dt></span></span> </dl>   |
| <span data-ttu-id="8787b-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="8787b-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="8787b-124"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8787b-124"><dt>Wiaguid.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8787b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8787b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8787b-126">**DEVICEDIALOGDATA**</span><span class="sxs-lookup"><span data-stu-id="8787b-126">**DEVICEDIALOGDATA**</span></span>](-wia-devicedialogdata.md)
</dt> </dl>

 

 




