---
description: 刪除用於連線身分識別的使用者認證。
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: 'DeleteConnectedIdentity 函式 (Indentitystore) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteConnectedIdentity
api_type:
- HeaderDef
api_location:
- Indentitystore.h
ms.openlocfilehash: 8079985f916e996a56b4203ad6ad065c1b7664e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026098"
---
# <a name="deleteconnectedidentity-function"></a><span data-ttu-id="c5430-103">DeleteConnectedIdentity 函式</span><span class="sxs-lookup"><span data-stu-id="c5430-103">DeleteConnectedIdentity function</span></span>

<span data-ttu-id="c5430-104">刪除用於連線身分識別的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="c5430-104">Deletes the user credential used for the connected identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5430-105">語法</span><span class="sxs-lookup"><span data-stu-id="c5430-105">Syntax</span></span>


```C++
SEC_ENTRY DeleteConnectedIdentity(
  _In_     PVOID  ProviderHandle,
  _In_opt_ HANDLE UserToken,
  _In_     PSID   UserSid,
  _In_     PWSTR  IdentityUserName
);
```



## <a name="parameters"></a><span data-ttu-id="c5430-106">參數</span><span class="sxs-lookup"><span data-stu-id="c5430-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5430-107">*ProviderHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5430-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5430-108">身分識別提供者控制碼。</span><span class="sxs-lookup"><span data-stu-id="c5430-108">Identity provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="c5430-109">*UserToken* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c5430-109">*UserToken* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c5430-110">已連線使用者的權杖，其帳戶將會轉換為本機帳戶。</span><span class="sxs-lookup"><span data-stu-id="c5430-110">Token of the connected user whose account is going to be converted to a local account.</span></span> <span data-ttu-id="c5430-111">如果 *UserToken* 不是 **Null**，則身分識別提供者會使用此權杖來載入使用者設定檔，並清除連接的狀態。</span><span class="sxs-lookup"><span data-stu-id="c5430-111">If *UserToken* is not **NULL**, the identity provider uses this token to load the user profile and clean up connected states.</span></span> <span data-ttu-id="c5430-112">如果 *UserToken* 為 **Null**，LSA 會強制中斷連接。</span><span class="sxs-lookup"><span data-stu-id="c5430-112">If *UserToken* is **NULL**, LSA is forcing the disconnection.</span></span> <span data-ttu-id="c5430-113">身分識別提供者應清除此使用者的任何全域線上狀態，但提供者不需要清除使用者設定檔中的線上狀態。</span><span class="sxs-lookup"><span data-stu-id="c5430-113">The identity provider should clean up any global connected states on this user, but the provider does not have to clean up connected states in the user profile.</span></span>

</dd> <dt>

<span data-ttu-id="c5430-114">*UserSid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5430-114">*UserSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5430-115">已連線使用者的主要 SID。</span><span class="sxs-lookup"><span data-stu-id="c5430-115">The primary SID of the connected user.</span></span> <span data-ttu-id="c5430-116">如果 *UserToken* 不是 **Null**，這個參數就是 token 的使用者 SID。</span><span class="sxs-lookup"><span data-stu-id="c5430-116">If *UserToken* is not **NULL**, this parameter is the user SID of the token.</span></span> <span data-ttu-id="c5430-117">如果 *UserToken* 為 **Null**，則會使用此參數來識別已連接的使用者，並清除該使用者的全域連接狀態。</span><span class="sxs-lookup"><span data-stu-id="c5430-117">If *UserToken* is **NULL**, this parameter is used to identify the connected user and clean up global connected states of that user.</span></span>

</dd> <dt>

<span data-ttu-id="c5430-118">*IdentityUserName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5430-118">*IdentityUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5430-119">身分識別的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="c5430-119">The user name of the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5430-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5430-120">Return value</span></span>

<span data-ttu-id="c5430-121">如果函式成功，則函式會傳回 SEC \_ E \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c5430-121">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="c5430-122">如果函式失敗，函數可能會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c5430-122">If the function fails, the function may return one of the following error codes.</span></span>



| <span data-ttu-id="c5430-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5430-123">Return value</span></span>                                                                                               | <span data-ttu-id="c5430-124">描述</span><span class="sxs-lookup"><span data-stu-id="c5430-124">Description</span></span>                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5430-125"><dt>狀態 \_ 不正確 \_ 參數</dt></span><span class="sxs-lookup"><span data-stu-id="c5430-125"><dt>STATUS\_INVALID\_PARAMETER</dt></span></span> </dl>      | <span data-ttu-id="c5430-126">參數無效。</span><span class="sxs-lookup"><span data-stu-id="c5430-126">A parameter is not valid.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="c5430-127"><dt>\_沒有 \_ 這類 \_ 使用者的狀態</dt></span><span class="sxs-lookup"><span data-stu-id="c5430-127"><dt>STATUS\_NO\_SUCH\_USER</dt></span></span> </dl>          | <span data-ttu-id="c5430-128">*UserSid* 所識別的使用者不存在、目前尚未連接，或沒有使用者名稱符合 *IdentityUserName* 的身分識別。</span><span class="sxs-lookup"><span data-stu-id="c5430-128">The user identified by *UserSid* does not exist, is not currently connected, or there is no identity whose user name matches *IdentityUserName*.</span></span><br/> |
| <dl> <span data-ttu-id="c5430-129"><dt>狀態 \_ 不足的 \_ 資源</dt></span><span class="sxs-lookup"><span data-stu-id="c5430-129"><dt>STATUS\_INSUFFICIENT\_RESOURCES</dt></span></span> </dl> | <span data-ttu-id="c5430-130">沒有足夠的記憶體可處理要求。</span><span class="sxs-lookup"><span data-stu-id="c5430-130">There is not enough memory to process the request.</span></span><br/>                                                                                               |



 

## <a name="requirements"></a><span data-ttu-id="c5430-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5430-131">Requirements</span></span>



| <span data-ttu-id="c5430-132">需求</span><span class="sxs-lookup"><span data-stu-id="c5430-132">Requirement</span></span> | <span data-ttu-id="c5430-133">值</span><span class="sxs-lookup"><span data-stu-id="c5430-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5430-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5430-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c5430-135">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5430-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="c5430-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5430-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c5430-137">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5430-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5430-138">標頭</span><span class="sxs-lookup"><span data-stu-id="c5430-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5430-139"><dt>Indentitystore。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5430-139"><dt>Indentitystore.h</dt></span></span> </dl> |



 

 




