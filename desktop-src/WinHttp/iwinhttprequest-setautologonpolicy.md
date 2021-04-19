---
description: 設定目前的自動登入原則。
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: IWinHttpRequest：： SetAutoLogonPolicy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetAutoLogonPolicy
- WinHttpRequest.SetAutoLogonPolicy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: cad8bd0080d10a1395a0a9d275951ff961a60bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991902"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a><span data-ttu-id="6ac02-103">IWinHttpRequest：： SetAutoLogonPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="6ac02-103">IWinHttpRequest::SetAutoLogonPolicy method</span></span>

<span data-ttu-id="6ac02-104">**SetAutoLogonPolicy** 方法會設定目前的 [自動登入原則](authentication-in-winhttp.md)。</span><span class="sxs-lookup"><span data-stu-id="6ac02-104">The **SetAutoLogonPolicy** method sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac02-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ac02-105">Syntax</span></span>


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="6ac02-106">參數</span><span class="sxs-lookup"><span data-stu-id="6ac02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ac02-107">*AutoLogonPolicy* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ac02-107">*AutoLogonPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ac02-108">指定目前的自動登入原則。</span><span class="sxs-lookup"><span data-stu-id="6ac02-108">Specifies the current automatic logon policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ac02-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ac02-109">Return value</span></span>

<span data-ttu-id="6ac02-110">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="6ac02-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ac02-111">備註</span><span class="sxs-lookup"><span data-stu-id="6ac02-111">Remarks</span></span>

<span data-ttu-id="6ac02-112">預設原則是 [**AutoLogonPolicy \_ OnlyIfBypassProxy**](winhttprequestautologonpolicy.md)。</span><span class="sxs-lookup"><span data-stu-id="6ac02-112">The default policy is [**AutoLogonPolicy\_OnlyIfBypassProxy**](winhttprequestautologonpolicy.md).</span></span>

<span data-ttu-id="6ac02-113">呼叫 **SetAutoLogonPolicy** ，在呼叫 [**send**](iwinhttprequest-send.md) 以傳送要求之前，設定自動登入原則。</span><span class="sxs-lookup"><span data-stu-id="6ac02-113">Call **SetAutoLogonPolicy** to set the automatic logon policy before calling [**Send**](iwinhttprequest-send.md) to send the request.</span></span>

> [!Note]  
> <span data-ttu-id="6ac02-114">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="6ac02-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="6ac02-115">範例</span><span class="sxs-lookup"><span data-stu-id="6ac02-115">Examples</span></span>

<span data-ttu-id="6ac02-116">下列腳本範例示範如何將自動登入原則設定為永遠不會使用 NTLM 或協商驗證。</span><span class="sxs-lookup"><span data-stu-id="6ac02-116">The following scripting example shows how to set the automatic logon policy to never use NTLM or Negotiate authentication automatically.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Do not automatically send user credentials.
HttpReq.SetAutoLogonPolicy(2);

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="6ac02-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ac02-117">Requirements</span></span>



| <span data-ttu-id="6ac02-118">需求</span><span class="sxs-lookup"><span data-stu-id="6ac02-118">Requirement</span></span> | <span data-ttu-id="6ac02-119">值</span><span class="sxs-lookup"><span data-stu-id="6ac02-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac02-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ac02-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6ac02-121">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ac02-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="6ac02-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ac02-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6ac02-123">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="6ac02-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="6ac02-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6ac02-124">Redistributable</span></span><br/>          | <span data-ttu-id="6ac02-125">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="6ac02-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="6ac02-126">Idl</span><span class="sxs-lookup"><span data-stu-id="6ac02-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ac02-127"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ac02-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="6ac02-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="6ac02-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ac02-129"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ac02-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="6ac02-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6ac02-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ac02-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ac02-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6ac02-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ac02-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ac02-133">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="6ac02-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="6ac02-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="6ac02-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="6ac02-135">WinHTTP 中的驗證</span><span class="sxs-lookup"><span data-stu-id="6ac02-135">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="6ac02-136">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="6ac02-136">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




