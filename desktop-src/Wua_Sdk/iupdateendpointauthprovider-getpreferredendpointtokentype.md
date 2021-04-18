---
description: 傳回服務端點的慣用驗證 token 類型。
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: 'IUpdateEndpointAuthProvider：： GetPreferredEndpointTokenType 方法 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetPreferredEndpointTokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 670835ee3c2dfd01ae46a7cf78395959ea9a26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191477"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a><span data-ttu-id="5f2e8-103">IUpdateEndpointAuthProvider：： GetPreferredEndpointTokenType 方法</span><span class="sxs-lookup"><span data-stu-id="5f2e8-103">IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType method</span></span>

<span data-ttu-id="5f2e8-104">傳回服務端點的慣用驗證 token 類型。</span><span class="sxs-lookup"><span data-stu-id="5f2e8-104">Returns the preferred type of authentication token for the endpoint of the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f2e8-105">語法</span><span class="sxs-lookup"><span data-stu-id="5f2e8-105">Syntax</span></span>


```C++
HRESULT GetPreferredEndpointTokenType(
  [in]  GUID               serviceId,
  [in]  UpdateEndpointType endpointType,
  [in]  ULONG              ulRequestedTypes,
  [out] ULONG              *pulPreferredTokenTypes
);
```



## <a name="parameters"></a><span data-ttu-id="5f2e8-106">參數</span><span class="sxs-lookup"><span data-stu-id="5f2e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f2e8-107">*serviceId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f2e8-107">*serviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f2e8-108">識別要更新的服務。</span><span class="sxs-lookup"><span data-stu-id="5f2e8-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="5f2e8-109">*endpointType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f2e8-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f2e8-110">識別要連接到服務的端點 tneeded 型別。</span><span class="sxs-lookup"><span data-stu-id="5f2e8-110">Identifies the type of endpoint tneeded to connect to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5f2e8-111">*ulRequestedTypes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f2e8-111">*ulRequestedTypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f2e8-112">識別端點所支援的一組 Or 運算 token。</span><span class="sxs-lookup"><span data-stu-id="5f2e8-112">Identifies the ORed set of tokens that are supported by the endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="5f2e8-113">*pulPreferredTokenTypes* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5f2e8-113">*pulPreferredTokenTypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f2e8-114">指定慣用之驗證 token 類型的 Or 運算集。</span><span class="sxs-lookup"><span data-stu-id="5f2e8-114">Specify the ORed set of authentication token types that are preferred.</span></span> <span data-ttu-id="5f2e8-115"> (設定為0，表示不需要驗證權杖) 。</span><span class="sxs-lookup"><span data-stu-id="5f2e8-115">(Set to 0 to indicate that no authentication token is needed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f2e8-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f2e8-116">Return value</span></span>

<span data-ttu-id="5f2e8-117">\_如果成功，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="5f2e8-117">Returns S\_OK if successful.</span></span> <span data-ttu-id="5f2e8-118">否則，會傳回 COM 或 Windows 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5f2e8-118">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f2e8-119">備註</span><span class="sxs-lookup"><span data-stu-id="5f2e8-119">Remarks</span></span>

<span data-ttu-id="5f2e8-120">當傳回此方法時，WUA 會從慣用的類型中選擇 token 類型，並將它傳遞至 [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) 方法的 tokenType 參數。</span><span class="sxs-lookup"><span data-stu-id="5f2e8-120">When this method is returned, WUA chooses a token type from the preferred types and passes it to the tokenType parameter of the [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f2e8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f2e8-121">Requirements</span></span>



| <span data-ttu-id="5f2e8-122">需求</span><span class="sxs-lookup"><span data-stu-id="5f2e8-122">Requirement</span></span> | <span data-ttu-id="5f2e8-123">值</span><span class="sxs-lookup"><span data-stu-id="5f2e8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f2e8-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f2e8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5f2e8-125">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f2e8-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="5f2e8-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f2e8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5f2e8-127">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="5f2e8-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="5f2e8-128">標頭</span><span class="sxs-lookup"><span data-stu-id="5f2e8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f2e8-129"><dt>UpdateEndpointAuth。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f2e8-129"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f2e8-130">Idl</span><span class="sxs-lookup"><span data-stu-id="5f2e8-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5f2e8-131"><dt>UpdateEndpointAuth .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5f2e8-131"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="5f2e8-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="5f2e8-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f2e8-133"><dt>UpdateEndpointAuth .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f2e8-133"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="5f2e8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5f2e8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f2e8-135"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f2e8-135"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f2e8-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f2e8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f2e8-137">**IUpdateEndpointAuthProvider**</span><span class="sxs-lookup"><span data-stu-id="5f2e8-137">**IUpdateEndpointAuthProvider**</span></span>](iupdateendpointauthprovider.md)
</dt> <dt>

[<span data-ttu-id="5f2e8-138">**GetEndpointToken**</span><span class="sxs-lookup"><span data-stu-id="5f2e8-138">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




