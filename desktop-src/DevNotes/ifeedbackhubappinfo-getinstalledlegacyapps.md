---
description: IFeedbackHubAppInfo：： GetInstalledLegacyApps 方法-此 API 無法供所有應用程式使用。 除非您的應用程式是由 Microsoft 特別布建，否則這些 Api 的呼叫將會在執行時間失敗。
ms.assetid: 84135D6F-8232-4CE5-AD38-D18823F0E174
title: IFeedbackHubAppInfo：： GetInstalledLegacyApps 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IFeedbackHubAppInfo.GetInstalledLegacyApps
api_type:
- COM
api_location: ''
ms.openlocfilehash: 167be3846322a1b3aacdf752374b9b0089220963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096696"
---
# <a name="ifeedbackhubappinfogetinstalledlegacyapps-method"></a><span data-ttu-id="1134e-104">IFeedbackHubAppInfo：： GetInstalledLegacyApps 方法</span><span class="sxs-lookup"><span data-stu-id="1134e-104">IFeedbackHubAppInfo::GetInstalledLegacyApps method</span></span>

<span data-ttu-id="1134e-105">所有應用程式都無法使用此 API。</span><span class="sxs-lookup"><span data-stu-id="1134e-105">This API is not available to all apps.</span></span> <span data-ttu-id="1134e-106">除非您的應用程式是由 Microsoft 特別布建，否則這些 Api 的呼叫將會在執行時間失敗。</span><span class="sxs-lookup"><span data-stu-id="1134e-106">Unless your app is specially provisioned by Microsoft, calls to these APIs will fail at runtime.</span></span>

## <a name="syntax"></a><span data-ttu-id="1134e-107">語法</span><span class="sxs-lookup"><span data-stu-id="1134e-107">Syntax</span></span>


```C++
virtual void GetInstalledLegacyApps(
  [out, optional] IObjectArray **result
);
```



## <a name="parameters"></a><span data-ttu-id="1134e-108">參數</span><span class="sxs-lookup"><span data-stu-id="1134e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1134e-109">*結果* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="1134e-109">*result* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1134e-110">所有應用程式都無法使用此 API。</span><span class="sxs-lookup"><span data-stu-id="1134e-110">This API is not available to all apps.</span></span> <span data-ttu-id="1134e-111">除非您的應用程式是由 Microsoft 特別布建，否則這些 Api 的呼叫將會在執行時間失敗。</span><span class="sxs-lookup"><span data-stu-id="1134e-111">Unless your app is specially provisioned by Microsoft, calls to these APIs will fail at runtime.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1134e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1134e-112">Return value</span></span>

<span data-ttu-id="1134e-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1134e-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1134e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1134e-114">Requirements</span></span>



| <span data-ttu-id="1134e-115">需求</span><span class="sxs-lookup"><span data-stu-id="1134e-115">Requirement</span></span> | <span data-ttu-id="1134e-116">值</span><span class="sxs-lookup"><span data-stu-id="1134e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1134e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1134e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1134e-118">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1134e-118">Windows 10 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1134e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1134e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1134e-120">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1134e-120">Windows Server 2016 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1134e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1134e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1134e-122">**IFeedbackHubAppInfo**</span><span class="sxs-lookup"><span data-stu-id="1134e-122">**IFeedbackHubAppInfo**</span></span>](ifeebackhubappinfo.md)
</dt> </dl>

 

 




