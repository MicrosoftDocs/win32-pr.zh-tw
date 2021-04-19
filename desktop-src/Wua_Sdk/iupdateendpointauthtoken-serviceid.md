---
description: 取得要使用端點 token 驗證的服務識別碼。
ms.assetid: FE110B8E-F8FB-4CC8-BDD8-6427BA8B7920
title: 'IUpdateEndpointAuthToken：： ServiceID 方法 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.ServiceID
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 8384baa0a4f8bb48e603e0f2f8bed417e783b7f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981141"
---
# <a name="iupdateendpointauthtokenserviceid-method"></a><span data-ttu-id="fc429-103">IUpdateEndpointAuthToken：： ServiceID 方法</span><span class="sxs-lookup"><span data-stu-id="fc429-103">IUpdateEndpointAuthToken::ServiceID method</span></span>

<span data-ttu-id="fc429-104">取得要使用端點 token 驗證的服務識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc429-104">Gets the identifier of the service to be authenticated with the endpoint token.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc429-105">語法</span><span class="sxs-lookup"><span data-stu-id="fc429-105">Syntax</span></span>


```C++
HRESULT ServiceID(
  [out] GUID *pServiceID
);
```



## <a name="parameters"></a><span data-ttu-id="fc429-106">參數</span><span class="sxs-lookup"><span data-stu-id="fc429-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc429-107">*pServiceID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fc429-107">*pServiceID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc429-108">服務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc429-108">The identifier of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc429-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc429-109">Return value</span></span>

<span data-ttu-id="fc429-110">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="fc429-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="fc429-111">否則，會傳回 COM 或 Windows 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fc429-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc429-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc429-112">Requirements</span></span>



| <span data-ttu-id="fc429-113">需求</span><span class="sxs-lookup"><span data-stu-id="fc429-113">Requirement</span></span> | <span data-ttu-id="fc429-114">值</span><span class="sxs-lookup"><span data-stu-id="fc429-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc429-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc429-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fc429-116">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc429-116">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="fc429-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc429-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fc429-118">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="fc429-118">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="fc429-119">標頭</span><span class="sxs-lookup"><span data-stu-id="fc429-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc429-120"><dt>UpdateEndpointAuth。h</dt></span><span class="sxs-lookup"><span data-stu-id="fc429-120"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc429-121">Idl</span><span class="sxs-lookup"><span data-stu-id="fc429-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fc429-122"><dt>UpdateEndpointAuth .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fc429-122"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="fc429-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="fc429-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc429-124"><dt>UpdateEndpointAuth .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc429-124"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="fc429-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fc429-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc429-126"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc429-126"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc429-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc429-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc429-128">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="fc429-128">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




