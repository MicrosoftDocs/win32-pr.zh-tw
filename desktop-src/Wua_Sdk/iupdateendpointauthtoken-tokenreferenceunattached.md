---
description: 取得標記之未附加參考的 XML 格式。
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: 'IUpdateEndpointAuthToken：： TokenReferenceUnattached 方法 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceUnattached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 7f9a25c444cf1ba8421d3787a9ead242750e5756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966731"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a><span data-ttu-id="7cd9e-103">IUpdateEndpointAuthToken：： TokenReferenceUnattached 方法</span><span class="sxs-lookup"><span data-stu-id="7cd9e-103">IUpdateEndpointAuthToken::TokenReferenceUnattached method</span></span>

<span data-ttu-id="7cd9e-104">取得標記之未附加參考的 XML 格式。</span><span class="sxs-lookup"><span data-stu-id="7cd9e-104">Gets the XML format of an unattached reference to the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd9e-105">語法</span><span class="sxs-lookup"><span data-stu-id="7cd9e-105">Syntax</span></span>


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a><span data-ttu-id="7cd9e-106">參數</span><span class="sxs-lookup"><span data-stu-id="7cd9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd9e-107">*pszTokenReference* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7cd9e-107">*pszTokenReference* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd9e-108">未附加之標記參考的指標。</span><span class="sxs-lookup"><span data-stu-id="7cd9e-108">Pointer to the unattached token reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd9e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7cd9e-109">Return value</span></span>

<span data-ttu-id="7cd9e-110">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="7cd9e-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="7cd9e-111">否則，會傳回 COM 或 Windows 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7cd9e-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd9e-112">備註</span><span class="sxs-lookup"><span data-stu-id="7cd9e-112">Remarks</span></span>

<span data-ttu-id="7cd9e-113">未附加的參考參考了 referece (，例如使用權杖) 的 signiture，而該權杖不在標記所在的訊息中。</span><span class="sxs-lookup"><span data-stu-id="7cd9e-113">An unattached reference refers a referece (such as the signiture that is using the token) that is not in the message where the token resides.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd9e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7cd9e-114">Requirements</span></span>



| <span data-ttu-id="7cd9e-115">需求</span><span class="sxs-lookup"><span data-stu-id="7cd9e-115">Requirement</span></span> | <span data-ttu-id="7cd9e-116">值</span><span class="sxs-lookup"><span data-stu-id="7cd9e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd9e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7cd9e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd9e-118">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cd9e-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="7cd9e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7cd9e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd9e-120">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="7cd9e-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="7cd9e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7cd9e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cd9e-122"><dt>UpdateEndpointAuth。h</dt></span><span class="sxs-lookup"><span data-stu-id="7cd9e-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="7cd9e-123">Idl</span><span class="sxs-lookup"><span data-stu-id="7cd9e-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7cd9e-124"><dt>UpdateEndpointAuth .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7cd9e-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="7cd9e-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="7cd9e-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="7cd9e-126"><dt>UpdateEndpointAuth .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cd9e-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="7cd9e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7cd9e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cd9e-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cd9e-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cd9e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7cd9e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd9e-130">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="7cd9e-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




