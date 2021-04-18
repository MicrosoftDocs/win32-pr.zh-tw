---
title: IWMDRMLicenseManagement 介面
description: IWMDRMLicenseManagement 介面提供的方法會執行與本機授權存放相關的一般作業。若要取得這個介面的實例，請呼叫 IWMDRMProvider CreateObject。 將 IID \_ IWMDRMLicenseManagement 傳遞為 riid 參數。
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- IWMDRMLicenseManagement 介面 windows 媒體格式
- IWMDRMLicenseManagement 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14a7c555200e2eac99def75a1ad8c1d5dc1223fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312482"
---
# <a name="iwmdrmlicensemanagement-interface"></a><span data-ttu-id="8810d-106">IWMDRMLicenseManagement 介面</span><span class="sxs-lookup"><span data-stu-id="8810d-106">IWMDRMLicenseManagement interface</span></span>

<span data-ttu-id="8810d-107">**IWMDRMLicenseManagement** 介面提供的方法會執行與本機授權存放相關的一般作業。</span><span class="sxs-lookup"><span data-stu-id="8810d-107">The **IWMDRMLicenseManagement** interface provides methods that perform general operations related to the local license store.</span></span>

<span data-ttu-id="8810d-108">若要取得這個介面的實例，請呼叫 [**IWMDRMProvider：： CreateObject**](iwmdrmprovider-createobject.md)。</span><span class="sxs-lookup"><span data-stu-id="8810d-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="8810d-109">將 **IID \_ IWMDRMLicenseManagement** 傳遞為 *riid* 參數。</span><span class="sxs-lookup"><span data-stu-id="8810d-109">Pass **IID\_IWMDRMLicenseManagement** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="8810d-110">成員</span><span class="sxs-lookup"><span data-stu-id="8810d-110">Members</span></span>

<span data-ttu-id="8810d-111">**IWMDRMLicenseManagement** 介面繼承自 [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)。</span><span class="sxs-lookup"><span data-stu-id="8810d-111">The **IWMDRMLicenseManagement** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="8810d-112">**IWMDRMLicenseManagement** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8810d-112">**IWMDRMLicenseManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="8810d-113">方法</span><span class="sxs-lookup"><span data-stu-id="8810d-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8810d-114">方法</span><span class="sxs-lookup"><span data-stu-id="8810d-114">Methods</span></span>

<span data-ttu-id="8810d-115">**IWMDRMLicenseManagement** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8810d-115">The **IWMDRMLicenseManagement** interface has these methods.</span></span>



| <span data-ttu-id="8810d-116">方法</span><span class="sxs-lookup"><span data-stu-id="8810d-116">Method</span></span>                                                                                               | <span data-ttu-id="8810d-117">描述</span><span class="sxs-lookup"><span data-stu-id="8810d-117">Description</span></span>                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8810d-118">**AcquireLicense**</span><span class="sxs-lookup"><span data-stu-id="8810d-118">**AcquireLicense**</span></span>](iwmdrmlicensemanagement-acquirelicense.md)                                     | <span data-ttu-id="8810d-119">以非同步方式從指定的 URL 取得授權。</span><span class="sxs-lookup"><span data-stu-id="8810d-119">Asynchronously acquires a license from a specified URL.</span></span><br/>                                                      |
| [<span data-ttu-id="8810d-120">**BackupLicenses**</span><span class="sxs-lookup"><span data-stu-id="8810d-120">**BackupLicenses**</span></span>](iwmdrmlicensemanagement-backuplicenses.md)                                     | <span data-ttu-id="8810d-121">在本機授權存放區中建立授權的備份。</span><span class="sxs-lookup"><span data-stu-id="8810d-121">Creates a backup of the licenses in the local license store.</span></span><br/>                                                 |
| [<span data-ttu-id="8810d-122">**CleanLicenseStore**</span><span class="sxs-lookup"><span data-stu-id="8810d-122">**CleanLicenseStore**</span></span>](iwmdrmlicensemanagement-cleanlicensestore.md)                               | <span data-ttu-id="8810d-123">從授權存放區移除標記的授權，並重組存放區以改善效能。</span><span class="sxs-lookup"><span data-stu-id="8810d-123">Removes marked licenses from the license store and defragments the store to improve performance.</span></span><br/>             |
| [<span data-ttu-id="8810d-124">**CreateLicenseEnumeration**</span><span class="sxs-lookup"><span data-stu-id="8810d-124">**CreateLicenseEnumeration**</span></span>](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | <span data-ttu-id="8810d-125">根據參數值，建立以授權資訊填入的授權列舉值物件。</span><span class="sxs-lookup"><span data-stu-id="8810d-125">Creates a license enumerator object populated with license information based on parameter values.</span></span><br/>            |
| [<span data-ttu-id="8810d-126">**CreateLicenseRevocationChallenge**</span><span class="sxs-lookup"><span data-stu-id="8810d-126">**CreateLicenseRevocationChallenge**</span></span>](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | <span data-ttu-id="8810d-127">產生授權撤銷挑戰。</span><span class="sxs-lookup"><span data-stu-id="8810d-127">Generates a license revocation challenge.</span></span><br/>                                                                    |
| [<span data-ttu-id="8810d-128">**DeleteLicense**</span><span class="sxs-lookup"><span data-stu-id="8810d-128">**DeleteLicense**</span></span>](iwmdrmlicensemanagement-deletelicense.md)                                       | <span data-ttu-id="8810d-129">從暫時的本機授權存放區刪除授權。</span><span class="sxs-lookup"><span data-stu-id="8810d-129">Deletes a license from the temporary local license store.</span></span><br/>                                                    |
| [<span data-ttu-id="8810d-130">**MonitorLicenseAcquisition**</span><span class="sxs-lookup"><span data-stu-id="8810d-130">**MonitorLicenseAcquisition**</span></span>](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | <span data-ttu-id="8810d-131">開始監視授權取得程式。</span><span class="sxs-lookup"><span data-stu-id="8810d-131">Initiates monitoring for a license acquisition process.</span></span><br/>                                                      |
| [<span data-ttu-id="8810d-132">**ProcessLicenseDeletionMessage**</span><span class="sxs-lookup"><span data-stu-id="8810d-132">**ProcessLicenseDeletionMessage**</span></span>](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | <span data-ttu-id="8810d-133">刪除匯入的授權，以供原本以另一個內容保護系統保護的內容使用。</span><span class="sxs-lookup"><span data-stu-id="8810d-133">Deletes a license that was imported for content originally protected with another content protection system.</span></span><br/> |
| [<span data-ttu-id="8810d-134">**ProcessLicenseRevocationResponse**</span><span class="sxs-lookup"><span data-stu-id="8810d-134">**ProcessLicenseRevocationResponse**</span></span>](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | <span data-ttu-id="8810d-135">撤銷本機授權存放區的授權。</span><span class="sxs-lookup"><span data-stu-id="8810d-135">Revokes licenses from the local license store.</span></span><br/>                                                               |
| [<span data-ttu-id="8810d-136">**RestoreLicenses**</span><span class="sxs-lookup"><span data-stu-id="8810d-136">**RestoreLicenses**</span></span>](iwmdrmlicensemanagement-restorelicenses.md)                                   | <span data-ttu-id="8810d-137">還原先前備份的授權。</span><span class="sxs-lookup"><span data-stu-id="8810d-137">Restores previously backed up licenses.</span></span><br/>                                                                      |
| [<span data-ttu-id="8810d-138">**StoreLicense**</span><span class="sxs-lookup"><span data-stu-id="8810d-138">**StoreLicense**</span></span>](iwmdrmlicensemanagement-storelicense.md)                                         | <span data-ttu-id="8810d-139">將授權新增至本機授權存放區。</span><span class="sxs-lookup"><span data-stu-id="8810d-139">Adds a license to the local license store.</span></span><br/>                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="8810d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8810d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8810d-141">**介面**</span><span class="sxs-lookup"><span data-stu-id="8810d-141">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="8810d-142">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="8810d-142">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





