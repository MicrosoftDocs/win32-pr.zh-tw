---
description: 發出命令給 Windows 映像取得 (WIA) 2.0 硬體裝置。
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: 'IWiaItem2：:D eviceCommand 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceCommand
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2961a3c0e0d1b75a487b9bf112e76bee8c937a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972050"
---
# <a name="iwiaitem2devicecommand-method"></a><span data-ttu-id="bc530-103">IWiaItem2：:D eviceCommand 方法</span><span class="sxs-lookup"><span data-stu-id="bc530-103">IWiaItem2::DeviceCommand method</span></span>

<span data-ttu-id="bc530-104">發出命令給 Windows 映像取得 (WIA) 2.0 硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="bc530-104">Issues a command to a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc530-105">語法</span><span class="sxs-lookup"><span data-stu-id="bc530-105">Syntax</span></span>


```C++
HRESULT DeviceCommand(
  [in]            LONG      lFlags,
  [in]      const GUID      *pCmdGUID,
  [in, out]       IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="bc530-106">參數</span><span class="sxs-lookup"><span data-stu-id="bc530-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc530-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc530-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc530-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="bc530-108">Type: **LONG**</span></span>

<span data-ttu-id="bc530-109">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="bc530-109">Currently unused.</span></span> <span data-ttu-id="bc530-110">應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="bc530-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="bc530-111">*pCmdGUID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc530-111">*pCmdGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc530-112">類型： \**CONST GUID \** _</span><span class="sxs-lookup"><span data-stu-id="bc530-112">Type: \**const GUID\** _</span></span>

<span data-ttu-id="bc530-113">指定要傳送至 WIA 2.0 裝置的命令。</span><span class="sxs-lookup"><span data-stu-id="bc530-113">Specifies the command to send to the WIA 2.0 device.</span></span> <span data-ttu-id="bc530-114">請參閱 [_ *WIA 裝置命令* \*](-wia-wia-device-commands.md)。</span><span class="sxs-lookup"><span data-stu-id="bc530-114">See [_ *WIA Device Commands*\*](-wia-wia-device-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc530-115">*ppIWiaItem2* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="bc530-115">*ppIWiaItem2* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc530-116">類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="bc530-116">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="bc530-117">接收命令所建立之 [**IWiaItem2**](-wia-iwiaitem2.md) 專案的指標位址（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="bc530-117">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) item created by the command, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc530-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc530-118">Return value</span></span>

<span data-ttu-id="bc530-119">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bc530-119">Type: **HRESULT**</span></span>

<span data-ttu-id="bc530-120">除了標準 COM 錯誤碼之外，此方法可能會傳回下列值。</span><span class="sxs-lookup"><span data-stu-id="bc530-120">In addition to the standard COM error codes, the method may return the following value.</span></span>



| <span data-ttu-id="bc530-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bc530-121">Return code</span></span>                                                                                       | <span data-ttu-id="bc530-122">Description</span><span class="sxs-lookup"><span data-stu-id="bc530-122">Description</span></span>                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bc530-123"><dt>**E \_ CMDNOTSUPPORTED**</dt></span><span class="sxs-lookup"><span data-stu-id="bc530-123"><dt>**E\_CMDNOTSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="bc530-124">此命令不會針對呼叫方法的 [**IWiaItem2**](-wia-iwiaitem2.md) 介面來執行。</span><span class="sxs-lookup"><span data-stu-id="bc530-124">The command is not implemented for the [**IWiaItem2**](-wia-iwiaitem2.md) interface on which the method is called.</span></span> <span data-ttu-id="bc530-125">尚未定義此錯誤的數值。</span><span class="sxs-lookup"><span data-stu-id="bc530-125">The numeric value for this error is not yet defined.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="bc530-126">備註</span><span class="sxs-lookup"><span data-stu-id="bc530-126">Remarks</span></span>

<span data-ttu-id="bc530-127">這個方法的行為會根據呼叫方法的節點類別而有所不同。</span><span class="sxs-lookup"><span data-stu-id="bc530-127">The behavior of this method is different depending on the category of the node on which the method is called.</span></span>

<span data-ttu-id="bc530-128">當應用程式使用 **IWiaItem2：:D evicecommand** 方法來傳送 [**WIA \_ CMD \_ TAKE \_ PICTURE**](-wia-wia-device-commands.md)命令至裝置時，WIA 2.0 執行時間系統會建立 [**IWiaItem2**](-wia-iwiaitem2.md)物件來代表影像。</span><span class="sxs-lookup"><span data-stu-id="bc530-128">When the application sends the [**WIA\_CMD\_TAKE\_PICTURE**](-wia-wia-device-commands.md) command to the device using the **IWiaItem2::DeviceCommand** method, the WIA 2.0 run-time system creates an [**IWiaItem2**](-wia-iwiaitem2.md) object to represent the image.</span></span> <span data-ttu-id="bc530-129">**IWiaItem2：:D evicecommand** 方法會將介面的位址儲存在 *ppIWiaItem2* 參數中。</span><span class="sxs-lookup"><span data-stu-id="bc530-129">The **IWiaItem2::DeviceCommand** method stores the address of the interface in the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="bc530-130">應用程式必須在透過 *ppIWiaItem2* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="bc530-130">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc530-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc530-131">Requirements</span></span>



| <span data-ttu-id="bc530-132">需求</span><span class="sxs-lookup"><span data-stu-id="bc530-132">Requirement</span></span> | <span data-ttu-id="bc530-133">值</span><span class="sxs-lookup"><span data-stu-id="bc530-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bc530-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc530-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bc530-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc530-135">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bc530-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc530-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bc530-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc530-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bc530-138">標頭</span><span class="sxs-lookup"><span data-stu-id="bc530-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc530-139"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="bc530-139"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc530-140">Idl</span><span class="sxs-lookup"><span data-stu-id="bc530-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bc530-141"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bc530-141"><dt>Wia.idl</dt></span></span> </dl> |



 

 
