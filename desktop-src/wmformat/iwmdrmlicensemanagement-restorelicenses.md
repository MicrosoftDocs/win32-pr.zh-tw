---
title: 'IWMDRMLicenseManagement RestoreLicenses 方法 (Wmdrmsdk .h) '
description: RestoreLicenses 方法會從藉由呼叫 BackupLicenses 方法所建立的授權備份還原授權。
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- RestoreLicenses 方法 windows Media 格式
- RestoreLicenses 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，RestoreLicenses 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.RestoreLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb07f3989ff19faa723e4b1d1cd50dc4e269f219
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977694"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a><span data-ttu-id="9c631-106">IWMDRMLicenseManagement：： RestoreLicenses 方法</span><span class="sxs-lookup"><span data-stu-id="9c631-106">IWMDRMLicenseManagement::RestoreLicenses method</span></span>

<span data-ttu-id="9c631-107">**RestoreLicenses** 方法會從藉由呼叫 [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md)方法所建立的授權備份還原授權。</span><span class="sxs-lookup"><span data-stu-id="9c631-107">The **RestoreLicenses** method restores licenses from a license backup that was created by calling the [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c631-108">語法</span><span class="sxs-lookup"><span data-stu-id="9c631-108">Syntax</span></span>


```C++
HRESULT RestoreLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="9c631-109">參數</span><span class="sxs-lookup"><span data-stu-id="9c631-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c631-110">*bstrBackupDirectory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9c631-110">*bstrBackupDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c631-111">將從中還原授權之位置的 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="9c631-111">UNC path of the location from which the licenses will be restored.</span></span>

</dd> <dt>

<span data-ttu-id="9c631-112">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9c631-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c631-113">指定要使用之還原選項的旗標。</span><span class="sxs-lookup"><span data-stu-id="9c631-113">Flags specifying the restore options to use.</span></span> <span data-ttu-id="9c631-114">目前唯一支援的旗標是 WMDRM \_ RESTORE \_ 賦予，可在必要時將方法設定為執行還原的一部分。</span><span class="sxs-lookup"><span data-stu-id="9c631-114">The only flag currently supported is WMDRM\_RESTORE\_INDIVIDUALIZE, which configures the method to perform individualization as part of the restoration, if required.</span></span>

</dd> <dt>

<span data-ttu-id="9c631-115">*ppunkCancelationCookie* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9c631-115">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c631-116">指標，接收識別此非同步呼叫之物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="9c631-116">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="9c631-117">這個介面指標可透過呼叫 [**IWMDRMEventGenerator：： CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) 方法，用來取消非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="9c631-117">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c631-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c631-118">Return value</span></span>

<span data-ttu-id="9c631-119">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="9c631-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9c631-120">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="9c631-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9c631-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9c631-121">Return code</span></span>                                                                          | <span data-ttu-id="9c631-122">Description</span><span class="sxs-lookup"><span data-stu-id="9c631-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9c631-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9c631-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9c631-124">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="9c631-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9c631-125">備註</span><span class="sxs-lookup"><span data-stu-id="9c631-125">Remarks</span></span>

<span data-ttu-id="9c631-126">這個方法會以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="9c631-126">This method executes asynchronously.</span></span> <span data-ttu-id="9c631-127">它會在呼叫後立即傳回，然後在處理完成時產生一連串的 **MEWMDRMLicenseRestoreProgress** 事件，後面接著 **MEWMDRMLicenseRestoreCompleted** 事件。</span><span class="sxs-lookup"><span data-stu-id="9c631-127">It returns immediately after being called and then generates a series of **MEWMDRMLicenseRestoreProgress** events followed by an **MEWMDRMLicenseRestoreCompleted** event when processing is complete.</span></span> <span data-ttu-id="9c631-128">藉由呼叫 **IMFMediaEvent：： GetValue** 取得的每個 **MEWMDRMLicenseRestoreProgress** 事件的值都是 **IUnknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="9c631-128">The value of each of the **MEWMDRMLicenseRestoreProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="9c631-129">您可以呼叫所抓取 **IUnknown** 介面的 **QueryInterface** 方法，以取得 [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md)介面的實例。</span><span class="sxs-lookup"><span data-stu-id="9c631-129">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interface.</span></span>

<span data-ttu-id="9c631-130">如需使用 Windows Media DRM 用戶端擴充 Api 的非同步方法的詳細資訊，請參閱 [使用媒體基礎事件模型](using-the-media-foundation-model.md)。</span><span class="sxs-lookup"><span data-stu-id="9c631-130">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

<span data-ttu-id="9c631-131">備份可以來自本機電腦或不同的電腦。</span><span class="sxs-lookup"><span data-stu-id="9c631-131">The backup can be from the local machine or from a different machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c631-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c631-132">Requirements</span></span>



| <span data-ttu-id="9c631-133">需求</span><span class="sxs-lookup"><span data-stu-id="9c631-133">Requirement</span></span> | <span data-ttu-id="9c631-134">值</span><span class="sxs-lookup"><span data-stu-id="9c631-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c631-135">標頭</span><span class="sxs-lookup"><span data-stu-id="9c631-135">Header</span></span><br/>  | <dl> <span data-ttu-id="9c631-136"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="9c631-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c631-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="9c631-137">Library</span></span><br/> | <dl> <span data-ttu-id="9c631-138"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c631-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c631-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c631-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c631-140">**IWMDRMLicenseManagement 介面**</span><span class="sxs-lookup"><span data-stu-id="9c631-140">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





