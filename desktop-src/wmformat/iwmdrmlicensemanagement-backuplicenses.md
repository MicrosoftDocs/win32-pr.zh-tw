---
title: 'IWMDRMLicenseManagement BackupLicenses 方法 (Wmdrmsdk .h) '
description: BackupLicenses 方法會在本機授權存放區中建立授權的備份。
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- BackupLicenses 方法 windows Media 格式
- BackupLicenses 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，BackupLicenses 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.BackupLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c7f676b532353c839a428571f6d28540851bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987087"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a><span data-ttu-id="635e5-106">IWMDRMLicenseManagement：： BackupLicenses 方法</span><span class="sxs-lookup"><span data-stu-id="635e5-106">IWMDRMLicenseManagement::BackupLicenses method</span></span>

<span data-ttu-id="635e5-107">**BackupLicenses** 方法會在本機授權存放區中建立授權的備份。</span><span class="sxs-lookup"><span data-stu-id="635e5-107">The **BackupLicenses** method creates a backup of the licenses in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="635e5-108">語法</span><span class="sxs-lookup"><span data-stu-id="635e5-108">Syntax</span></span>


```C++
HRESULT BackupLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="635e5-109">參數</span><span class="sxs-lookup"><span data-stu-id="635e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="635e5-110">*bstrBackupDirectory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="635e5-110">*bstrBackupDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="635e5-111">將備份授權之目標位置的 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="635e5-111">UNC path of the location to which the licenses will be backed up.</span></span>

</dd> <dt>

<span data-ttu-id="635e5-112">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="635e5-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="635e5-113">旗標，指定要使用的備份選項。</span><span class="sxs-lookup"><span data-stu-id="635e5-113">Flags specifying the backup options to use.</span></span> <span data-ttu-id="635e5-114">目前唯一支援的旗標是 WMDRM \_ 備份 \_ 覆寫，它會設定方法以覆寫目錄中任何現有的備份檔案。</span><span class="sxs-lookup"><span data-stu-id="635e5-114">The only flag currently supported is WMDRM\_BACKUP\_OVERWRITE, which configures the method to overwrite any existing backup files in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="635e5-115">*ppunkCancelationCookie* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="635e5-115">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="635e5-116">指標，接收識別此非同步呼叫之物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="635e5-116">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="635e5-117">這個介面指標可透過呼叫 [**IWMDRMEventGenerator：： CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) 方法，用來取消非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="635e5-117">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="635e5-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="635e5-118">Return value</span></span>

<span data-ttu-id="635e5-119">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="635e5-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="635e5-120">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="635e5-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="635e5-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="635e5-121">Return code</span></span>                                                                          | <span data-ttu-id="635e5-122">Description</span><span class="sxs-lookup"><span data-stu-id="635e5-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="635e5-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="635e5-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="635e5-124">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="635e5-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="635e5-125">備註</span><span class="sxs-lookup"><span data-stu-id="635e5-125">Remarks</span></span>

<span data-ttu-id="635e5-126">這個方法會以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="635e5-126">This method executes asynchronously.</span></span> <span data-ttu-id="635e5-127">它會在呼叫後立即傳回，然後在處理完成時產生一連串的 **MEWMDRMLicenseBackupProgress** 事件，後面接著 **MEWMDRMLicenseBackupCompleted** 事件。</span><span class="sxs-lookup"><span data-stu-id="635e5-127">It returns immediately after being called and then generates a series of **MEWMDRMLicenseBackupProgress** events followed by an **MEWMDRMLicenseBackupCompleted** event when processing is complete.</span></span> <span data-ttu-id="635e5-128">藉由呼叫 **IMFMediaEvent：： GetValue** 取得的每個 **MEWMDRMLicenseBackupProgress** 事件的值都是 **IUnknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="635e5-128">The value of each of the **MEWMDRMLicenseBackupProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="635e5-129">您可以呼叫所抓取 **IUnknown** 介面的 **QueryInterface** 方法，以取得 [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md)介面的實例。</span><span class="sxs-lookup"><span data-stu-id="635e5-129">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interface.</span></span>

<span data-ttu-id="635e5-130">如需使用 Windows Media DRM 用戶端擴充 Api 的非同步方法的詳細資訊，請參閱 [使用媒體基礎事件模型](using-the-media-foundation-model.md)。</span><span class="sxs-lookup"><span data-stu-id="635e5-130">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

<span data-ttu-id="635e5-131">並非所有授權都可進行備份。</span><span class="sxs-lookup"><span data-stu-id="635e5-131">Not all licenses are permitted to be backed up.</span></span> <span data-ttu-id="635e5-132">這個方法只會備份允許的授權。</span><span class="sxs-lookup"><span data-stu-id="635e5-132">This method only backs up licenses that allow it.</span></span>

## <a name="requirements"></a><span data-ttu-id="635e5-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="635e5-133">Requirements</span></span>



| <span data-ttu-id="635e5-134">需求</span><span class="sxs-lookup"><span data-stu-id="635e5-134">Requirement</span></span> | <span data-ttu-id="635e5-135">值</span><span class="sxs-lookup"><span data-stu-id="635e5-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="635e5-136">標頭</span><span class="sxs-lookup"><span data-stu-id="635e5-136">Header</span></span><br/>  | <dl> <span data-ttu-id="635e5-137"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="635e5-137"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="635e5-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="635e5-138">Library</span></span><br/> | <dl> <span data-ttu-id="635e5-139"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="635e5-139"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="635e5-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="635e5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="635e5-141">**IWMDRMLicenseManagement 介面**</span><span class="sxs-lookup"><span data-stu-id="635e5-141">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





