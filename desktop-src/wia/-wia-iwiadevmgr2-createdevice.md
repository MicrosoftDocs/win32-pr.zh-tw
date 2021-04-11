---
description: 為 Windows 映像取得 (WIA) 2.0 裝置建立 IWiaItem2 物件的階層式樹狀結構。
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: 'IWiaDevMgr2：： CreateDevice 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.CreateDevice
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a548a0ef43c2621b77c4ed10acde393af21d596d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849358"
---
# <a name="iwiadevmgr2createdevice-method"></a><span data-ttu-id="99bdd-103">IWiaDevMgr2：： CreateDevice 方法</span><span class="sxs-lookup"><span data-stu-id="99bdd-103">IWiaDevMgr2::CreateDevice method</span></span>

<span data-ttu-id="99bdd-104">為 Windows 映像取得 (WIA) 2.0 裝置建立 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的階層式樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="99bdd-104">Creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for a Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="99bdd-105">語法</span><span class="sxs-lookup"><span data-stu-id="99bdd-105">Syntax</span></span>


```C++
HRESULT CreateDevice(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrDeviceID,
  [out] IWiaItem2 **ppWiaItem2Root
);
```



## <a name="parameters"></a><span data-ttu-id="99bdd-106">參數</span><span class="sxs-lookup"><span data-stu-id="99bdd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99bdd-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99bdd-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99bdd-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="99bdd-108">Type: **LONG**</span></span>

<span data-ttu-id="99bdd-109">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="99bdd-109">Currently unused.</span></span> <span data-ttu-id="99bdd-110">應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="99bdd-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="99bdd-111">*bstrDeviceID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99bdd-111">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99bdd-112">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="99bdd-112">Type: **BSTR**</span></span>

<span data-ttu-id="99bdd-113">指定 WIA 2.0 裝置的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="99bdd-113">Specifies the unique identifier of the WIA 2.0 device.</span></span>

</dd> <dt>

<span data-ttu-id="99bdd-114">*ppWiaItem2Root* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="99bdd-114">*ppWiaItem2Root* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99bdd-115">類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="99bdd-115">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="99bdd-116">接收指向 WIA 2.0 裝置之階層樹狀結構中根項目之 [**IWiaItem2**](-wia-iwiaitem2.md) 介面的指標位址。</span><span class="sxs-lookup"><span data-stu-id="99bdd-116">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item in the hierarchical tree for the WIA 2.0 device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99bdd-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="99bdd-117">Return value</span></span>

<span data-ttu-id="99bdd-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="99bdd-118">Type: **HRESULT**</span></span>

<span data-ttu-id="99bdd-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="99bdd-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="99bdd-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="99bdd-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="99bdd-121">備註</span><span class="sxs-lookup"><span data-stu-id="99bdd-121">Remarks</span></span>

<span data-ttu-id="99bdd-122">應用程式會使用 **IWiaDevMgr2：： CreateDevice** 方法，為 bstrDeviceID 參數所指定的 WIA 2.0 裝置建立裝置物件。</span><span class="sxs-lookup"><span data-stu-id="99bdd-122">Applications use the **IWiaDevMgr2::CreateDevice** method to create a device object for the WIA 2.0 devices specified by the bstrDeviceID parameter.</span></span> <span data-ttu-id="99bdd-123">當它傳回時， **IWiaDevMgr2：： CreateDevice** 方法會將指標的位址儲存在參數 *ppWiaItem2Root* 中，指向 **IWiaDevMgr2：： CreateDevice** 所建立 [**IWiaItem2**](-wia-iwiaitem2.md)物件樹狀結構的根專案。</span><span class="sxs-lookup"><span data-stu-id="99bdd-123">When it returns, the **IWiaDevMgr2::CreateDevice** method stores an address of a pointer in the parameter *ppWiaItem2Root*, which points to the root item of the tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects created by **IWiaDevMgr2::CreateDevice**.</span></span> <span data-ttu-id="99bdd-124">應用程式可以使用此物件樹狀結構來控制及取出 WIA 2.0 裝置的資料。</span><span class="sxs-lookup"><span data-stu-id="99bdd-124">Applications can use this tree of objects to control and retrieve data from the WIA 2.0 device.</span></span>

<span data-ttu-id="99bdd-125">應用程式必須在透過 *ppWiaItem2Root* 參數接收的指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="99bdd-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the pointers they receive through the *ppWiaItem2Root* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="99bdd-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="99bdd-126">Requirements</span></span>



| <span data-ttu-id="99bdd-127">需求</span><span class="sxs-lookup"><span data-stu-id="99bdd-127">Requirement</span></span> | <span data-ttu-id="99bdd-128">值</span><span class="sxs-lookup"><span data-stu-id="99bdd-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="99bdd-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99bdd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="99bdd-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99bdd-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="99bdd-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99bdd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="99bdd-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99bdd-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="99bdd-133">標頭</span><span class="sxs-lookup"><span data-stu-id="99bdd-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="99bdd-134"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="99bdd-134"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="99bdd-135">Idl</span><span class="sxs-lookup"><span data-stu-id="99bdd-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="99bdd-136"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="99bdd-136"><dt>Wia.idl</dt></span></span> </dl> |



 

 
