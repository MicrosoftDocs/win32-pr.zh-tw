---
description: 以 IStream 形式抓取回應實體主體。
ms.assetid: e12a9338-5e0c-4672-bbc6-31375b872e94
title: IWinHttpRequest：： ResponseStream 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseStream
- IWinHttpRequest.get_ResponseStream
- WinHttpRequest.ResponseStream
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: ec9f497e687c52735784a5e3edad01905ac7a6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194154"
---
# <a name="iwinhttprequestresponsestream-property"></a><span data-ttu-id="34b0f-103">IWinHttpRequest：： ResponseStream 屬性</span><span class="sxs-lookup"><span data-stu-id="34b0f-103">IWinHttpRequest::ResponseStream property</span></span>

<span data-ttu-id="34b0f-104">**ResponseStream** 屬性會將回應實體主體視為 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)。</span><span class="sxs-lookup"><span data-stu-id="34b0f-104">The **ResponseStream** property retrieves the response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span>

<span data-ttu-id="34b0f-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="34b0f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="34b0f-106">語法</span><span class="sxs-lookup"><span data-stu-id="34b0f-106">Syntax</span></span>


```C++
HRESULT get_ResponseStream(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseStream = WinHttpRequest.ResponseStream
```





## <a name="property-value"></a><span data-ttu-id="34b0f-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="34b0f-107">Property value</span></span>

<span data-ttu-id="34b0f-108">此 **變數** 會接收可針對 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面進行查詢的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面指標。</span><span class="sxs-lookup"><span data-stu-id="34b0f-108">A **Variant** that receives a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface that can be queried for an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> <span data-ttu-id="34b0f-109">此資料流程會傳回直接從伺服器接收的原始資料。</span><span class="sxs-lookup"><span data-stu-id="34b0f-109">This stream returns the raw data as received directly from the server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="34b0f-110">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="34b0f-110">Error codes</span></span>

<span data-ttu-id="34b0f-111">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="34b0f-111">The return value is **S\_OK** on success or an error value otherwise.</span></span>

<span data-ttu-id="34b0f-112">如果先前的 [**傳送**](iwinhttprequest-send.md)作業未完成，它將會是 **E \_ 暫** 止。</span><span class="sxs-lookup"><span data-stu-id="34b0f-112">It will be **E\_PENDING** if the previous [**Send**](iwinhttprequest-send.md) operation is not complete.</span></span>

## <a name="remarks"></a><span data-ttu-id="34b0f-113">備註</span><span class="sxs-lookup"><span data-stu-id="34b0f-113">Remarks</span></span>

<span data-ttu-id="34b0f-114">在傳回的指標上呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，以取得 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="34b0f-114">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the returned pointer to obtain a pointer to an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> <span data-ttu-id="34b0f-115">這個屬性會以 **IStream** 的形式傳迴響應資料。</span><span class="sxs-lookup"><span data-stu-id="34b0f-115">This property returns the response data as an **IStream**.</span></span> <span data-ttu-id="34b0f-116">這個屬性只能在呼叫 [**Send**](iwinhttprequest-send.md) 方法之後叫用。</span><span class="sxs-lookup"><span data-stu-id="34b0f-116">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="34b0f-117">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="34b0f-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="34b0f-118">範例</span><span class="sxs-lookup"><span data-stu-id="34b0f-118">Examples</span></span>

<span data-ttu-id="34b0f-119">下列範例示範如何開啟 HTTP 連接、傳送 HTTP 要求，以及將回應讀取為 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)。</span><span class="sxs-lookup"><span data-stu-id="34b0f-119">The following example shows how to open an HTTP connection, send an HTTP request, and read the response as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span> <span data-ttu-id="34b0f-120">**IStream** 中的資料會寫入檔案 Temp1.gif。</span><span class="sxs-lookup"><span data-stu-id="34b0f-120">The data from the **IStream** is written to the file Temp1.gif.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <objbase.h>

#include "httprequest.h"

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

// IID for IWinHttpRequest.
const IID IID_IWinHttpRequest =
{
  0x06f29373,
  0x5c5a,
  0x4b54,
  {0xb0, 0x25, 0x6e, 0xf1, 0xbf, 0x8a, 0xbf, 0x0e}
};

#define Trace(_s) fprintf(stderr, _s) 
#define TraceErr(_s, _hr) fprintf(stderr, _s, _hr) 
#define Check(_hr,_s) if (FAILED(_hr)) { fprintf(stderr, _s ## " 0x%08lx\n", _hr); return -1; }

int main(int argc, char* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    // Variable for return value.
    HRESULT    hr;

    // Initialize COM.
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;
    VARIANT            varResponse;

    VariantInit(&varResponse);
    
    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IWinHttpRequest, 
                              (void **)&pIWinHttpRequest);
    }

    // ==== Get binary (.gif) file and write it to disk. =========
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest for synchronous access.
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(
            L"https://www.microsoft.com/library/homepage/images/ms-banner.gif");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get response body.
        hr = pIWinHttpRequest->get_ResponseBody(&varResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to file temp1.gif.
        long UpperBounds;
        long LowerBounds;
        unsigned char* buff;
        // Verify that varResponse contains array of unsigned bytes.
        if (varResponse.vt == (VT_ARRAY | VT_UI1)) {
            long Dims = SafeArrayGetDim(varResponse.parray);
            // The array should only have 1 dimension.
            if (Dims == 1) {
                // Get upper and lower array bounds.
                SafeArrayGetLBound(varResponse.parray, 1, 
                                   &LowerBounds);
                SafeArrayGetUBound(varResponse.parray, 1, 
                                   &UpperBounds);
                UpperBounds++;
                // Lock SAFEARRAY for access.
                SafeArrayAccessData (varResponse.parray, 
                                     (void**)&buff);
                // Output array to file temp.gif.
                HANDLE hFile; 
                DWORD  dwBytesWritten;
                // Create file.
                hFile = CreateFile(TEXT("Temp1.gif"),     
                    GENERIC_WRITE,              // Open for writing. 
                    0,                          // Do not share. 
                    NULL,                       // No security. 
                    CREATE_ALWAYS,              // Overwrite existing.
                    FILE_ATTRIBUTE_NORMAL,      // Normal file.
                    NULL);                      // No attribute template.

                if (hFile == INVALID_HANDLE_VALUE) 
                    {
                    wprintf(L"Could not open file."); // Process error.
                    }
                else
                    {
                    WriteFile(hFile, buff, UpperBounds - LowerBounds, 
                        &dwBytesWritten, NULL); 
                    }
                CloseHandle(hFile);
                SafeArrayUnaccessData (varResponse.parray);
            }
        }    
    }

    // ======== Get binary (.gif) file and write 
    // it to disk using IStream. ================
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest for synchronous access.
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(
            L"https://www.microsoft.com/library/homepage/images/ms-banner.gif");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response as an IStream.
        hr = pIWinHttpRequest->get_ResponseStream(&varResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to file temp1.gif.
        IStream*    pStream = NULL; 
        BYTE        bBuffer[8192]; 
        DWORD       cb, cbRead, cbWritten; 
        // Check that an IStream was received.
        if (VT_UNKNOWN == V_VT(&varResponse) || 
            VT_STREAM == V_VT(&varResponse)) 
        { 
            // Get IStream interface pStream.
            hr = V_UNKNOWN(&varResponse)->QueryInterface(IID_IStream, 
                                 reinterpret_cast<void**>(&pStream)); 
            Check(hr, "QI for IStream"); 
        } 
        else 
        { 
            wprintf(L"Unexpected vartype for Response\n"); 
            return -1; 
        } 

        HANDLE hFile; 
        // Open file Temp2.gif for output.
        hFile = CreateFile(TEXT("Temp2.gif"),     
            GENERIC_WRITE,                // Open for writing. 
            0,                            // Do not share. 
            NULL,                         // No security. 
            CREATE_ALWAYS,                // Overwrite existing.
            FILE_ATTRIBUTE_NORMAL,        // Normal file.
            NULL);                        // No attribute template.
        if (hFile == INVALID_HANDLE_VALUE) 
            {
            wprintf(L"Could not open file.");  // Process error.
            }
        else
            {
            // Copy data from the response stream to file. 
            cb = sizeof(bBuffer); 
            hr = pStream->Read(bBuffer, cb, &cbRead); 
            while (SUCCEEDED(hr) && 0 != cbRead) 
                { 
                if (!WriteFile(hFile, bBuffer, 
                               cbRead, &cbWritten, NULL)) 
                    { 
                    TraceErr("WriteFile fails with 0x%08lx\n", 
                             HRESULT_FROM_WIN32(GetLastError())); 
                    return -1; 
                    } 
                hr = pStream->Read(bBuffer, cb, &cbRead); 
                } 
            }
        CloseHandle(hFile);
        pStream->Release(); 
        VariantClear(&varResponse); 
    }
    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);
    
    CoUninitialize();
    return 0;
}
```



## <a name="requirements"></a><span data-ttu-id="34b0f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="34b0f-121">Requirements</span></span>



| <span data-ttu-id="34b0f-122">需求</span><span class="sxs-lookup"><span data-stu-id="34b0f-122">Requirement</span></span> | <span data-ttu-id="34b0f-123">值</span><span class="sxs-lookup"><span data-stu-id="34b0f-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="34b0f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="34b0f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="34b0f-125">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34b0f-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="34b0f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="34b0f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="34b0f-127">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="34b0f-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="34b0f-128">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="34b0f-128">Redistributable</span></span><br/>          | <span data-ttu-id="34b0f-129">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="34b0f-129">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="34b0f-130">Idl</span><span class="sxs-lookup"><span data-stu-id="34b0f-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="34b0f-131"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="34b0f-131"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="34b0f-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="34b0f-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="34b0f-133"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="34b0f-133"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="34b0f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="34b0f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34b0f-135"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34b0f-135"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="34b0f-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34b0f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34b0f-137">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="34b0f-137">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="34b0f-138">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="34b0f-138">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="34b0f-139">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="34b0f-139">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)
</dt> <dt>

[<span data-ttu-id="34b0f-140">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="34b0f-140">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)
</dt> <dt>

[<span data-ttu-id="34b0f-141">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="34b0f-141">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

