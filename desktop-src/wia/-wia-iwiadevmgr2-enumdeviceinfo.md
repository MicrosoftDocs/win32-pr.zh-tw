---
description: 針對每個可用的 Windows 映像取得 (WIA) 2.0 裝置，建立屬性資訊的列舉值。
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: 'IWiaDevMgr2：： EnumDeviceInfo 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.EnumDeviceInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bd9e9281b625f4cec5377537d82a304045b95a3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691096"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a><span data-ttu-id="5e08d-103">IWiaDevMgr2：： EnumDeviceInfo 方法</span><span class="sxs-lookup"><span data-stu-id="5e08d-103">IWiaDevMgr2::EnumDeviceInfo method</span></span>

<span data-ttu-id="5e08d-104">針對每個可用的 Windows 映像取得 (WIA) 2.0 裝置，建立屬性資訊的列舉值。</span><span class="sxs-lookup"><span data-stu-id="5e08d-104">Creates an enumerator of property information for each available Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e08d-105">語法</span><span class="sxs-lookup"><span data-stu-id="5e08d-105">Syntax</span></span>


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="5e08d-106">參數</span><span class="sxs-lookup"><span data-stu-id="5e08d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e08d-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5e08d-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e08d-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="5e08d-108">Type: **LONG**</span></span>

<span data-ttu-id="5e08d-109">指定要列舉的 WIA 2.0 裝置類型。</span><span class="sxs-lookup"><span data-stu-id="5e08d-109">Specifies the type of WIA 2.0 devices to enumerate.</span></span>

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span data-ttu-id="5e08d-110"><span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA \_ >LNK-DEVINFO \_ 列舉 \_ 區域**</span><span class="sxs-lookup"><span data-stu-id="5e08d-110"><span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA\_DEVINFO\_ENUM\_LOCAL**</span></span>


</dt> <dd>

<span data-ttu-id="5e08d-111">只會列舉在本機連線的主動式掃描器裝置。</span><span class="sxs-lookup"><span data-stu-id="5e08d-111">Only locally connected active scanner devices are enumerated.</span></span>

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span data-ttu-id="5e08d-112"><span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA \_ >LNK-DEVINFO \_ 列舉 \_ 全部**</span><span class="sxs-lookup"><span data-stu-id="5e08d-112"><span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA\_DEVINFO\_ENUM\_ALL**</span></span>


</dt> <dd>

<span data-ttu-id="5e08d-113">所有裝置都會在本機和遠端列舉，包括非使用中 (中斷連線) 裝置和舊版 STI 裝置。</span><span class="sxs-lookup"><span data-stu-id="5e08d-113">All devices are enumerated, both locally and remote, including inactive (disconnected) devices and legacy STI-only devices.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5e08d-114">*ppIEnum* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="5e08d-114">*ppIEnum* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5e08d-115">類型： **[ **IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***</span><span class="sxs-lookup"><span data-stu-id="5e08d-115">Type: **[**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***</span></span>

<span data-ttu-id="5e08d-116">接收 [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) 介面之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="5e08d-116">Receives the address of a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e08d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e08d-117">Return value</span></span>

<span data-ttu-id="5e08d-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5e08d-118">Type: **HRESULT**</span></span>

<span data-ttu-id="5e08d-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5e08d-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5e08d-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5e08d-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e08d-121">備註</span><span class="sxs-lookup"><span data-stu-id="5e08d-121">Remarks</span></span>

<span data-ttu-id="5e08d-122">**IWiaDevMgr2：： EnumDeviceInfo** 方法會建立支援 [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)介面的列舉值物件。</span><span class="sxs-lookup"><span data-stu-id="5e08d-122">The **IWiaDevMgr2::EnumDeviceInfo** method creates an enumerator object that supports the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span> <span data-ttu-id="5e08d-123">方法會在參數 *ppIEnum* 中儲存 **IEnumWIA \_ DEV \_ INFO** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5e08d-123">The method stores a pointer to the **IEnumWIA\_DEV\_INFO** interface in the parameter *ppIEnum*.</span></span> <span data-ttu-id="5e08d-124">應用程式可以使用 **IEnumWIA \_ DEV \_ INFO** 介面指標來列舉附加至使用者電腦的每個 WIA 2.0 裝置的屬性。</span><span class="sxs-lookup"><span data-stu-id="5e08d-124">Applications can use the **IEnumWIA\_DEV\_INFO** interface pointer to enumerate the properties of each WIA 2.0 device attached to the user's computer.</span></span>

<span data-ttu-id="5e08d-125">應用程式必須在透過 *ppIEnum* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="5e08d-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e08d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e08d-126">Requirements</span></span>



| <span data-ttu-id="5e08d-127">需求</span><span class="sxs-lookup"><span data-stu-id="5e08d-127">Requirement</span></span> | <span data-ttu-id="5e08d-128">值</span><span class="sxs-lookup"><span data-stu-id="5e08d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e08d-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e08d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5e08d-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e08d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5e08d-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e08d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5e08d-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e08d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5e08d-133">標頭</span><span class="sxs-lookup"><span data-stu-id="5e08d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e08d-134"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="5e08d-134"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e08d-135">Idl</span><span class="sxs-lookup"><span data-stu-id="5e08d-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e08d-136"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e08d-136"><dt>Wia.idl</dt></span></span> </dl> |



 

 
