---
description: 選取要傳送至安全超文字傳輸通訊協定 (HTTPS) 伺服器的用戶端憑證。
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: IWinHttpRequest：： SetClientCertificate 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetClientCertificate
- WinHttpRequest.SetClientCertificate
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0b346451e87b62116d7202b476e554c84604ea48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319859"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a><span data-ttu-id="89a78-103">IWinHttpRequest：： SetClientCertificate 方法</span><span class="sxs-lookup"><span data-stu-id="89a78-103">IWinHttpRequest::SetClientCertificate method</span></span>

<span data-ttu-id="89a78-104">**SetClientCertificate** 方法會選取要傳送至安全超文字傳輸通訊協定 (HTTPS) server 的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="89a78-104">The **SetClientCertificate** method selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="89a78-105">語法</span><span class="sxs-lookup"><span data-stu-id="89a78-105">Syntax</span></span>


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a><span data-ttu-id="89a78-106">參數</span><span class="sxs-lookup"><span data-stu-id="89a78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89a78-107">*ClientCertificate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89a78-107">*ClientCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89a78-108">指定用戶端憑證的位置、 [*憑證存放區*](glossary.md)和主體。</span><span class="sxs-lookup"><span data-stu-id="89a78-108">Specifies the location, [*certificate store*](glossary.md), and subject of a client certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89a78-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="89a78-109">Return value</span></span>

<span data-ttu-id="89a78-110">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="89a78-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="89a78-111">備註</span><span class="sxs-lookup"><span data-stu-id="89a78-111">Remarks</span></span>

<span data-ttu-id="89a78-112">*ClientCertificate* 參數中指定的字串包含以反斜線分隔的憑證位置、憑證存放區和主體名稱。</span><span class="sxs-lookup"><span data-stu-id="89a78-112">The string specified in the *ClientCertificate* parameter consists of the certificate location, certificate store, and subject name delimited by backslashes.</span></span> <span data-ttu-id="89a78-113">如需有關憑證字串元件的詳細資訊，請參閱 [用戶端憑證](ssl-in-winhttp.md)。</span><span class="sxs-lookup"><span data-stu-id="89a78-113">For more information about the components of the certificate string, see [Client Certificates](ssl-in-winhttp.md).</span></span>

<span data-ttu-id="89a78-114">憑證存放區名稱和位置是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="89a78-114">The certificate store name and location are optional.</span></span> <span data-ttu-id="89a78-115">但是，如果您指定憑證存放區，您也必須指定該憑證存放區的位置。</span><span class="sxs-lookup"><span data-stu-id="89a78-115">However, if you specify a certificate store, you must also specify the location of that certificate store.</span></span> <span data-ttu-id="89a78-116">預設位置是 [目前 \_ 使用者]，預設憑證存放區為 [我的]。</span><span class="sxs-lookup"><span data-stu-id="89a78-116">The default location is CURRENT\_USER and the default certificate store is "MY".</span></span> <span data-ttu-id="89a78-117">空白的主旨表示應使用憑證存放區中的第一個憑證。</span><span class="sxs-lookup"><span data-stu-id="89a78-117">A blank subject indicates that the first certificate in the certificate store should be used.</span></span>

<span data-ttu-id="89a78-118">呼叫 **SetClientCertificate** 來選取憑證，然後再呼叫 [**send**](iwinhttprequest-send.md) 以傳送要求。</span><span class="sxs-lookup"><span data-stu-id="89a78-118">Call **SetClientCertificate** to select a certificate before calling [**Send**](iwinhttprequest-send.md) to send the request.</span></span>

<span data-ttu-id="89a78-119">Microsoft Windows HTTP Services (WinHTTP) 不提供用戶端憑證給要求憑證進行驗證的 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="89a78-119">Microsoft Windows HTTP Services (WinHTTP) does not provide client certificates to proxy servers that request certificates for authentication.</span></span>

> [!Note]  
> <span data-ttu-id="89a78-120">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="89a78-120">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="89a78-121">範例</span><span class="sxs-lookup"><span data-stu-id="89a78-121">Examples</span></span>

<span data-ttu-id="89a78-122">下列腳本範例示範如何選取要隨要求傳送的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="89a78-122">The following scripting example shows how to select a client certificate to send with a request.</span></span> <span data-ttu-id="89a78-123">在 **HKEY \_ 本機 \_ 電腦** 的登錄中，從登錄中的 [個人] 憑證存放區選擇具有「我的 Middle-Tier 憑證」主體的憑證。</span><span class="sxs-lookup"><span data-stu-id="89a78-123">A certificate with the subject "My Middle-Tier Certificate" is chosen from the "Personal" certificate store in the registry under **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="89a78-124">因為此程式碼範例是 Microsoft JScript 專屬的，使用反斜線作為 escape 字元，所以需要兩個連續的反斜線來分隔憑證字串的元件。</span><span class="sxs-lookup"><span data-stu-id="89a78-124">Because this code example is specific to Microsoft JScript, which uses the backslash as an escape character, two adjacent backslashes are required to delimit components of the certificate string.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Select a client certificate.
HttpReq.SetClientCertificate(
            "LOCAL_MACHINE\\Personal\\My Middle-Tier Certificate");

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="89a78-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="89a78-125">Requirements</span></span>



| <span data-ttu-id="89a78-126">需求</span><span class="sxs-lookup"><span data-stu-id="89a78-126">Requirement</span></span> | <span data-ttu-id="89a78-127">值</span><span class="sxs-lookup"><span data-stu-id="89a78-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a78-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89a78-128">Minimum supported client</span></span><br/> | <span data-ttu-id="89a78-129">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89a78-129">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="89a78-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89a78-130">Minimum supported server</span></span><br/> | <span data-ttu-id="89a78-131">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="89a78-131">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="89a78-132">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="89a78-132">Redistributable</span></span><br/>          | <span data-ttu-id="89a78-133">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="89a78-133">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="89a78-134">Idl</span><span class="sxs-lookup"><span data-stu-id="89a78-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="89a78-135"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="89a78-135"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="89a78-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="89a78-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="89a78-137"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="89a78-137"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="89a78-138">DLL</span><span class="sxs-lookup"><span data-stu-id="89a78-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89a78-139"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89a78-139"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="89a78-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89a78-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a78-141">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="89a78-141">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="89a78-142">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="89a78-142">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="89a78-143">WinHTTP 中的 SSL</span><span class="sxs-lookup"><span data-stu-id="89a78-143">SSL in WinHTTP</span></span>](ssl-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="89a78-144">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="89a78-144">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




