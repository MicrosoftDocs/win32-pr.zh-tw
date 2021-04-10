---
description: 使用指定的認證，要求服務端點的權杖。
ms.assetid: 2CA0F826-9A05-4385-AF1A-A8C05B3DAFE2
title: 'IUpdateEndpointAuthProvider：： GetEndpointToken 方法 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetEndpointToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 55efe38ce9782b691e1ad32f7a21f6124e1f0bf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690716"
---
# <a name="iupdateendpointauthprovidergetendpointtoken-method"></a><span data-ttu-id="6b275-103">IUpdateEndpointAuthProvider：： GetEndpointToken 方法</span><span class="sxs-lookup"><span data-stu-id="6b275-103">IUpdateEndpointAuthProvider::GetEndpointToken method</span></span>

<span data-ttu-id="6b275-104">使用指定的認證，要求服務端點的權杖。</span><span class="sxs-lookup"><span data-stu-id="6b275-104">Request a token for the endpoint of the service using the specified credentials.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b275-105">語法</span><span class="sxs-lookup"><span data-stu-id="6b275-105">Syntax</span></span>


```C++
HRESULT GetEndpointToken(
  [in]  GUID                        serviceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  UpdateEndpointAuthTokenType tokenType,
  [in]  BOOL                        fRefreshOnline,
  [out] IUnknown                    **ppEndpointToken
);
```



## <a name="parameters"></a><span data-ttu-id="6b275-106">參數</span><span class="sxs-lookup"><span data-stu-id="6b275-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b275-107">*serviceId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6b275-107">*serviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b275-108">識別要更新的服務。</span><span class="sxs-lookup"><span data-stu-id="6b275-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="6b275-109">*endpointType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6b275-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b275-110">識別服務所執行之端點的類型。</span><span class="sxs-lookup"><span data-stu-id="6b275-110">Identifies the type of endpoint that is implemented by the service.</span></span>

</dd> <dt>

<span data-ttu-id="6b275-111">*proxySettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6b275-111">*proxySettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b275-112">連接至 proxy 伺服器時所要使用的設定。</span><span class="sxs-lookup"><span data-stu-id="6b275-112">The settings to be used when connecting to a proxy server.</span></span> <span data-ttu-id="6b275-113">如需詳細資訊，請參閱 [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="6b275-113">See the [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) structure for more details.</span></span>

</dd> <dt>

<span data-ttu-id="6b275-114">*hUserToken* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6b275-114">*hUserToken* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6b275-115">*tokenType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6b275-115">*tokenType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b275-116">識別用於驗證的驗證權杖類型。</span><span class="sxs-lookup"><span data-stu-id="6b275-116">Identifies the type of authentication token that is used for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="6b275-117">*fRefreshOnline* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6b275-117">*fRefreshOnline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b275-118">表示氣象 WUA 要求新的權杖。</span><span class="sxs-lookup"><span data-stu-id="6b275-118">Indicates weather WUA requests a new token.</span></span> <span data-ttu-id="6b275-119">True 表示要求新的權杖。</span><span class="sxs-lookup"><span data-stu-id="6b275-119">True indicates that a new token is requested.</span></span> <span data-ttu-id="6b275-120">False 表示要求新的或快取的標記。</span><span class="sxs-lookup"><span data-stu-id="6b275-120">False indicates that a new or cached token is requested.</span></span> <span data-ttu-id="6b275-121">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="6b275-121">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="6b275-122">*ppEndpointToken* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6b275-122">*ppEndpointToken* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b275-123">指定要使用的端點權杖。</span><span class="sxs-lookup"><span data-stu-id="6b275-123">Specifiy the endpoint token to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b275-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b275-124">Return value</span></span>

<span data-ttu-id="6b275-125">\_如果成功，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="6b275-125">Returns S\_OK if successful.</span></span> <span data-ttu-id="6b275-126">否則，會傳回 COM 或 Windows 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6b275-126">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b275-127">備註</span><span class="sxs-lookup"><span data-stu-id="6b275-127">Remarks</span></span>

<span data-ttu-id="6b275-128">WUA 通常會在第一次呼叫此方法時，將 fRefreshOnline 參數設定為 false，然後如果連接錯誤時 WUA，則會在再次呼叫方法時將該參數設定為 true。</span><span class="sxs-lookup"><span data-stu-id="6b275-128">WUA typically sets the fRefreshOnline parameter to false when this method is first called, then if a connection error occures WUA sets that parameter to true when the method is called again.</span></span> <span data-ttu-id="6b275-129">不過，此方法的執行可以從安全性權杖服務 (STS) 要求新的權杖，或隨時提供快取的權杖。</span><span class="sxs-lookup"><span data-stu-id="6b275-129">However, the implementation of this method can request a new token from a Security Token Service (STS) or provide a cached token at any time.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b275-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b275-130">Requirements</span></span>



| <span data-ttu-id="6b275-131">需求</span><span class="sxs-lookup"><span data-stu-id="6b275-131">Requirement</span></span> | <span data-ttu-id="6b275-132">值</span><span class="sxs-lookup"><span data-stu-id="6b275-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b275-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b275-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6b275-134">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b275-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="6b275-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b275-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6b275-136">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="6b275-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="6b275-137">標頭</span><span class="sxs-lookup"><span data-stu-id="6b275-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b275-138"><dt>UpdateEndpointAuth。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b275-138"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b275-139">Idl</span><span class="sxs-lookup"><span data-stu-id="6b275-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6b275-140"><dt>UpdateEndpointAuth .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6b275-140"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="6b275-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="6b275-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="6b275-142"><dt>UpdateEndpointAuth .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b275-142"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="6b275-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6b275-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b275-144"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b275-144"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b275-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b275-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b275-146">**IUpdateEndpointAuthProvider**</span><span class="sxs-lookup"><span data-stu-id="6b275-146">**IUpdateEndpointAuthProvider**</span></span>](iupdateendpointauthprovider.md)
</dt> </dl>

 

 




