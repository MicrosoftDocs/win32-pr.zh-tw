---
description: 取得用來加密權杖所保護之外寄訊息的索引鍵。
ms.assetid: 1ADBDFC8-E4D9-440B-B310-913213086283
title: 'IUpdateEndpointAuthToken：： SigningKey 方法 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.SigningKey
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: ae9847eb698bfcf0402a550ecb54705c4b3f3a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026273"
---
# <a name="iupdateendpointauthtokensigningkey-method"></a><span data-ttu-id="61b90-103">IUpdateEndpointAuthToken：： SigningKey 方法</span><span class="sxs-lookup"><span data-stu-id="61b90-103">IUpdateEndpointAuthToken::SigningKey method</span></span>

<span data-ttu-id="61b90-104">取得用來加密權杖所保護之外寄訊息的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="61b90-104">Gets the key that is used to encrypt the outgoing messages that the token protects.</span></span>

## <a name="syntax"></a><span data-ttu-id="61b90-105">語法</span><span class="sxs-lookup"><span data-stu-id="61b90-105">Syntax</span></span>


```C++
HRESULT SigningKey(
  [in, out, unique] BYTE  *pbKey,
  [in, out]         ULONG *pcbKeySize
);
```



## <a name="parameters"></a><span data-ttu-id="61b90-106">參數</span><span class="sxs-lookup"><span data-stu-id="61b90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61b90-107">*pbKey* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="61b90-107">*pbKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="61b90-108">用來加密外寄訊息的金鑰。</span><span class="sxs-lookup"><span data-stu-id="61b90-108">Key used to encrypt outgoing message.</span></span>

</dd> <dt>

<span data-ttu-id="61b90-109">*pcbKeySize* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="61b90-109">*pcbKeySize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="61b90-110">*Pbkey* 參數所參考的索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="61b90-110">Size of the key referenced by the *pbkey* paremeter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61b90-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="61b90-111">Return value</span></span>

<span data-ttu-id="61b90-112">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="61b90-112">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="61b90-113">否則，會傳回 COM 或 Windows 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="61b90-113">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="61b90-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="61b90-114">Requirements</span></span>



| <span data-ttu-id="61b90-115">需求</span><span class="sxs-lookup"><span data-stu-id="61b90-115">Requirement</span></span> | <span data-ttu-id="61b90-116">值</span><span class="sxs-lookup"><span data-stu-id="61b90-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61b90-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61b90-117">Minimum supported client</span></span><br/> | <span data-ttu-id="61b90-118">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61b90-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="61b90-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61b90-119">Minimum supported server</span></span><br/> | <span data-ttu-id="61b90-120">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="61b90-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="61b90-121">標頭</span><span class="sxs-lookup"><span data-stu-id="61b90-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="61b90-122"><dt>UpdateEndpointAuth。h</dt></span><span class="sxs-lookup"><span data-stu-id="61b90-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="61b90-123">Idl</span><span class="sxs-lookup"><span data-stu-id="61b90-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61b90-124"><dt>UpdateEndpointAuth .idl</dt></span><span class="sxs-lookup"><span data-stu-id="61b90-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="61b90-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="61b90-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="61b90-126"><dt>UpdateEndpointAuth .lib</dt></span><span class="sxs-lookup"><span data-stu-id="61b90-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="61b90-127">DLL</span><span class="sxs-lookup"><span data-stu-id="61b90-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61b90-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61b90-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61b90-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61b90-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b90-130">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="61b90-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




