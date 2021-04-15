---
description: 建立枚舉器，用來確定 Windows 映像取得 (WIA) 2.0 裝置支援的命令和事件。
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: 'IWiaItem2：： EnumDeviceCapabilities 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumDeviceCapabilities
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3e771aa636b42d9cd7e4024a1684ebe3edf02eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511640"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a><span data-ttu-id="5c2e5-103">IWiaItem2：： EnumDeviceCapabilities 方法</span><span class="sxs-lookup"><span data-stu-id="5c2e5-103">IWiaItem2::EnumDeviceCapabilities method</span></span>

<span data-ttu-id="5c2e5-104">建立枚舉器，用來確定 Windows 映像取得 (WIA) 2.0 裝置支援的命令和事件。</span><span class="sxs-lookup"><span data-stu-id="5c2e5-104">Creates an enumerator that is used to ascertain the commands and events a Windows Image Acquisition (WIA) 2.0 device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c2e5-105">語法</span><span class="sxs-lookup"><span data-stu-id="5c2e5-105">Syntax</span></span>


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a><span data-ttu-id="5c2e5-106">參數</span><span class="sxs-lookup"><span data-stu-id="5c2e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c2e5-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c2e5-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c2e5-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="5c2e5-108">Type: **LONG**</span></span>

<span data-ttu-id="5c2e5-109">指定旗標，以選取要列舉的功能類型。</span><span class="sxs-lookup"><span data-stu-id="5c2e5-109">Specifies a flag that selects the type of capabilities to enumerate.</span></span> <span data-ttu-id="5c2e5-110">這是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5c2e5-110">It is one of the following values.</span></span>

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span data-ttu-id="5c2e5-111"><span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**WIA \_ 裝置 \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="5c2e5-111"><span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**WIA\_DEVICE\_COMMANDS**</span></span>


</dt> <dd>

<span data-ttu-id="5c2e5-112">列舉裝置命令。</span><span class="sxs-lookup"><span data-stu-id="5c2e5-112">Enumerate device commands.</span></span>

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span data-ttu-id="5c2e5-113"><span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**WIA \_ 裝置 \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="5c2e5-113"><span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**WIA\_DEVICE\_EVENTS**</span></span>


</dt> <dd>

<span data-ttu-id="5c2e5-114">列舉裝置事件。</span><span class="sxs-lookup"><span data-stu-id="5c2e5-114">Enumerate device events.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5c2e5-115">*ppIEnumWIA \_開發人員 \_ 帽* \[ 出\]</span><span class="sxs-lookup"><span data-stu-id="5c2e5-115">*ppIEnumWIA\_DEV\_CAPS* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c2e5-116">類型： **[ **IEnumWIA \_ DEV \_ cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span><span class="sxs-lookup"><span data-stu-id="5c2e5-116">Type: **[**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span></span>

<span data-ttu-id="5c2e5-117">接收這個方法所建立的 [**IEnumWIA \_ DEV \_ CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="5c2e5-117">Receives a pointer to the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface created by this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c2e5-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c2e5-118">Return value</span></span>

<span data-ttu-id="5c2e5-119">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5c2e5-119">Type: **HRESULT**</span></span>

<span data-ttu-id="5c2e5-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5c2e5-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5c2e5-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5c2e5-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c2e5-122">備註</span><span class="sxs-lookup"><span data-stu-id="5c2e5-122">Remarks</span></span>

<span data-ttu-id="5c2e5-123">這個方法是用來建立列舉值物件，以取得 WIA 2.0 裝置支援的一組命令和事件。</span><span class="sxs-lookup"><span data-stu-id="5c2e5-123">This method is used to create an enumerator object to obtain the set of commands and events that a WIA 2.0 device supports.</span></span> <span data-ttu-id="5c2e5-124">*LFlags* 參數是用來指定要列舉哪些種類的裝置功能。</span><span class="sxs-lookup"><span data-stu-id="5c2e5-124">The *lFlags* parameter is used to specify which kinds of device capabilities to enumerate.</span></span> <span data-ttu-id="5c2e5-125">**IWiaItem2：： EnumDeviceCapabilities** 方法會在 *ppIEnumWIA \_ DEV \_ CAPS* 參數中儲存列舉值物件的介面位址。</span><span class="sxs-lookup"><span data-stu-id="5c2e5-125">The **IWiaItem2::EnumDeviceCapabilities** method stores the address of the interface of the enumerator object in the *ppIEnumWIA\_DEV\_CAPS* parameter.</span></span>

<span data-ttu-id="5c2e5-126">此方法只能在裝置樹狀結構之 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的根項目上呼叫。</span><span class="sxs-lookup"><span data-stu-id="5c2e5-126">This method can only be called on the root item of [**IWiaItem2**](-wia-iwiaitem2.md) objects of a device tree.</span></span>

<span data-ttu-id="5c2e5-127">應用程式必須在透過 *ppIEnumWIA \_ DEV \_ cap* 參數所收到的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="5c2e5-127">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnumWIA\_DEV\_CAPS* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c2e5-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c2e5-128">Requirements</span></span>



| <span data-ttu-id="5c2e5-129">需求</span><span class="sxs-lookup"><span data-stu-id="5c2e5-129">Requirement</span></span> | <span data-ttu-id="5c2e5-130">值</span><span class="sxs-lookup"><span data-stu-id="5c2e5-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c2e5-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c2e5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5c2e5-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c2e5-132">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5c2e5-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c2e5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5c2e5-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c2e5-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5c2e5-135">標頭</span><span class="sxs-lookup"><span data-stu-id="5c2e5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c2e5-136"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="5c2e5-136"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c2e5-137">Idl</span><span class="sxs-lookup"><span data-stu-id="5c2e5-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c2e5-138"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c2e5-138"><dt>Wia.idl</dt></span></span> </dl> |



 

 
