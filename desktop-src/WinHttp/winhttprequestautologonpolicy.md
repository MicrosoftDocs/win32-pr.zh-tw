---
description: 包含自動登入原則的可能設定。
ms.assetid: dad4f6a7-8e84-4f4f-b962-4189e3dc01f7
title: WinHttpRequestAutoLogonPolicy 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestAutoLogonPolicy
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: dab3dc14dd194e36b9b4d1225f77161005b9d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974039"
---
# <a name="winhttprequestautologonpolicy-enumeration"></a><span data-ttu-id="bafc7-103">WinHttpRequestAutoLogonPolicy 列舉</span><span class="sxs-lookup"><span data-stu-id="bafc7-103">WinHttpRequestAutoLogonPolicy enumeration</span></span>

<span data-ttu-id="bafc7-104">**WinHttpRequestAutoLogonPolicy** 列舉包含 [自動登入原則](authentication-in-winhttp.md)的可能設定。</span><span class="sxs-lookup"><span data-stu-id="bafc7-104">The **WinHttpRequestAutoLogonPolicy** enumeration includes possible settings for the [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bafc7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bafc7-105">Syntax</span></span>


```C++
typedef enum WinHttpRequestAutoLogonPolicy { 
  AutoLogonPolicy_Always             = 0,
  AutoLogonPolicy_OnlyIfBypassProxy  = 1,
  AutoLogonPolicy_Never              = 2
} WinHttpRequestAutoLogonPolicy;
```



## <a name="constants"></a><span data-ttu-id="bafc7-106">常數</span><span class="sxs-lookup"><span data-stu-id="bafc7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bafc7-107"><span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**\_一律 AutoLogonPolicy**</span><span class="sxs-lookup"><span data-stu-id="bafc7-107"><span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy\_Always**</span></span>
</dt> <dd>

<span data-ttu-id="bafc7-108">系統會針對所有要求執行使用預設認證的已驗證登入。</span><span class="sxs-lookup"><span data-stu-id="bafc7-108">An authenticated log on, using the default credentials, is performed for all requests.</span></span>

</dd> <dt>

<span data-ttu-id="bafc7-109"><span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy \_ OnlyIfBypassProxy**</span><span class="sxs-lookup"><span data-stu-id="bafc7-109"><span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy\_OnlyIfBypassProxy**</span></span>
</dt> <dd>

<span data-ttu-id="bafc7-110">使用預設認證的已驗證登入，只會針對近端內部網路上的要求執行。</span><span class="sxs-lookup"><span data-stu-id="bafc7-110">An authenticated log on, using the default credentials, is performed only for requests on the local intranet.</span></span> <span data-ttu-id="bafc7-111">在目前的 proxy 設定中，近端內部網路會被視為 proxy 略過清單上的任何伺服器。</span><span class="sxs-lookup"><span data-stu-id="bafc7-111">The local intranet is considered to be any server on the proxy bypass list in the current proxy configuration.</span></span>

</dd> <dt>

<span data-ttu-id="bafc7-112"><span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy \_ 永不**</span><span class="sxs-lookup"><span data-stu-id="bafc7-112"><span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy\_Never**</span></span>
</dt> <dd>

<span data-ttu-id="bafc7-113">不會自動使用驗證。</span><span class="sxs-lookup"><span data-stu-id="bafc7-113">Authentication is not used automatically.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bafc7-114">備註</span><span class="sxs-lookup"><span data-stu-id="bafc7-114">Remarks</span></span>

<span data-ttu-id="bafc7-115">若要設定自動登入原則，請呼叫 [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) 方法，並指定上述其中一個常數。</span><span class="sxs-lookup"><span data-stu-id="bafc7-115">To set the automatic logon policy, call the [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) method and specify one of the preceding constants.</span></span>

> [!Note]  
> <span data-ttu-id="bafc7-116">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="bafc7-116">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bafc7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bafc7-117">Requirements</span></span>



| <span data-ttu-id="bafc7-118">需求</span><span class="sxs-lookup"><span data-stu-id="bafc7-118">Requirement</span></span> | <span data-ttu-id="bafc7-119">值</span><span class="sxs-lookup"><span data-stu-id="bafc7-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="bafc7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bafc7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bafc7-121">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bafc7-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="bafc7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bafc7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bafc7-123">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="bafc7-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="bafc7-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="bafc7-124">Redistributable</span></span><br/>          | <span data-ttu-id="bafc7-125">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="bafc7-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="bafc7-126">Idl</span><span class="sxs-lookup"><span data-stu-id="bafc7-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bafc7-127"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bafc7-127"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bafc7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bafc7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bafc7-129">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="bafc7-129">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




