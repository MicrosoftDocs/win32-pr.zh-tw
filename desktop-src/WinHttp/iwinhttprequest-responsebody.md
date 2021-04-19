---
description: 以不帶正負號的位元組陣列形式捕獲回應實體主體。
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: IWinHttpRequest：： ResponseBody 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseBody
- IWinHttpRequest.get_ResponseBody
- WinHttpRequest.ResponseBody
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5a608f2744ad2880ecf7c4862b03821afcef9630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981210"
---
# <a name="iwinhttprequestresponsebody-property"></a><span data-ttu-id="4cc0e-103">IWinHttpRequest：： ResponseBody 屬性</span><span class="sxs-lookup"><span data-stu-id="4cc0e-103">IWinHttpRequest::ResponseBody property</span></span>

<span data-ttu-id="4cc0e-104">**ResponseBody** 屬性會以不帶正負號的位元組陣列形式抓取回應實體主體。</span><span class="sxs-lookup"><span data-stu-id="4cc0e-104">The **ResponseBody** property retrieves the response entity body as an array of unsigned bytes.</span></span>

<span data-ttu-id="4cc0e-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="4cc0e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cc0e-106">語法</span><span class="sxs-lookup"><span data-stu-id="4cc0e-106">Syntax</span></span>


```C++
HRESULT get_ResponseBody(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseBody = WinHttpRequest.ResponseBody
```





## <a name="property-value"></a><span data-ttu-id="4cc0e-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="4cc0e-107">Property value</span></span>

<span data-ttu-id="4cc0e-108">以不帶正負號的位元組陣列形式接收回應實體主體的 **變異** 值。</span><span class="sxs-lookup"><span data-stu-id="4cc0e-108">A **Variant** value that receives the response entity body as an array of unsigned bytes.</span></span> <span data-ttu-id="4cc0e-109">此陣列包含直接從伺服器接收的原始資料。</span><span class="sxs-lookup"><span data-stu-id="4cc0e-109">This array contains the raw data as received directly from the server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4cc0e-110">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="4cc0e-110">Error codes</span></span>

<span data-ttu-id="4cc0e-111">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="4cc0e-111">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cc0e-112">備註</span><span class="sxs-lookup"><span data-stu-id="4cc0e-112">Remarks</span></span>

<span data-ttu-id="4cc0e-113">這個屬性會傳回不帶正負號之位元組陣列中的回應資料。</span><span class="sxs-lookup"><span data-stu-id="4cc0e-113">This property returns the response data in an array of unsigned bytes.</span></span> <span data-ttu-id="4cc0e-114">如果回應沒有回應主體，則會傳回空的 variant。</span><span class="sxs-lookup"><span data-stu-id="4cc0e-114">If the response does not have a response body, an empty variant is returned.</span></span> <span data-ttu-id="4cc0e-115">這個屬性只能在呼叫 [**Send**](iwinhttprequest-send.md) 方法之後叫用。</span><span class="sxs-lookup"><span data-stu-id="4cc0e-115">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="4cc0e-116">如需 Windows XP 和 Windows 2000 之執行的詳細資訊，請參閱 [執行時間需求](winhttp-start-page.md)。</span><span class="sxs-lookup"><span data-stu-id="4cc0e-116">For more information about implementation for Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4cc0e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cc0e-117">Requirements</span></span>



| <span data-ttu-id="4cc0e-118">需求</span><span class="sxs-lookup"><span data-stu-id="4cc0e-118">Requirement</span></span> | <span data-ttu-id="4cc0e-119">值</span><span class="sxs-lookup"><span data-stu-id="4cc0e-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cc0e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4cc0e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4cc0e-121">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cc0e-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="4cc0e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4cc0e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4cc0e-123">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="4cc0e-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="4cc0e-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4cc0e-124">Redistributable</span></span><br/>          | <span data-ttu-id="4cc0e-125">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4cc0e-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="4cc0e-126">Idl</span><span class="sxs-lookup"><span data-stu-id="4cc0e-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4cc0e-127"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4cc0e-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="4cc0e-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="4cc0e-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="4cc0e-129"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cc0e-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="4cc0e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4cc0e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cc0e-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cc0e-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4cc0e-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4cc0e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc0e-133">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4cc0e-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="4cc0e-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4cc0e-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="4cc0e-135">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="4cc0e-135">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)
</dt> <dt>

[<span data-ttu-id="4cc0e-136">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="4cc0e-136">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)
</dt> <dt>

[<span data-ttu-id="4cc0e-137">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="4cc0e-137">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




