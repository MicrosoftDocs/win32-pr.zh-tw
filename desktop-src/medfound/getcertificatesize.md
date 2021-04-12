---
description: 取得顯示驅動程式憑證的大小。
ms.assetid: fd52e939-127a-4493-8406-31f7767921cd
title: GetCertificateSize 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateSize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bcd1f49ce65978c6a89c89cee1fda38e41434065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317959"
---
# <a name="getcertificatesize-function"></a><span data-ttu-id="da1e2-103">GetCertificateSize 函式</span><span class="sxs-lookup"><span data-stu-id="da1e2-103">GetCertificateSize function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da1e2-104">[輸出保護管理員](output-protection-manager.md)會使用此函式 (OPM) 來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="da1e2-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="da1e2-105">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="da1e2-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="da1e2-106">取得顯示驅動程式憑證的大小。</span><span class="sxs-lookup"><span data-stu-id="da1e2-106">Gets the size of a certificate for a display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="da1e2-107">語法</span><span class="sxs-lookup"><span data-stu-id="da1e2-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCertificateSize(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ ULONG                    *pulCertificateLength
);
```



## <a name="parameters"></a><span data-ttu-id="da1e2-108">參數</span><span class="sxs-lookup"><span data-stu-id="da1e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da1e2-109">*pstrDeviceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da1e2-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da1e2-110">[**UNICODE \_ 字串**](/windows/win32/api/subauth/ns-subauth-unicode_string)結構的指標，其中包含 [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa)函式所傳回之顯示裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="da1e2-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="da1e2-111">*ctPVPCertificateType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da1e2-111">*ctPVPCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da1e2-112">憑證的類型，指定為 **DXGKMDT \_ 憑證 \_ 類型** 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="da1e2-112">The type of certificate, specified as a member of the **DXGKMDT\_CERTIFICATE\_TYPE** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="da1e2-113">*pulCertificateLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="da1e2-113">*pulCertificateLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da1e2-114">接收憑證的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="da1e2-114">Receives the size of the certificate, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da1e2-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="da1e2-115">Return value</span></span>

<span data-ttu-id="da1e2-116">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="da1e2-116">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="da1e2-117">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="da1e2-117">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="da1e2-118">備註</span><span class="sxs-lookup"><span data-stu-id="da1e2-118">Remarks</span></span>

<span data-ttu-id="da1e2-119">應用程式應該呼叫 [**IOPMVideoOutput：： StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) 方法，而不是此函數。</span><span class="sxs-lookup"><span data-stu-id="da1e2-119">Applications should call the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method instead of this function.</span></span>

<span data-ttu-id="da1e2-120">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="da1e2-120">This function has no associated import library.</span></span> <span data-ttu-id="da1e2-121">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="da1e2-121">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="da1e2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="da1e2-122">Requirements</span></span>



| <span data-ttu-id="da1e2-123">需求</span><span class="sxs-lookup"><span data-stu-id="da1e2-123">Requirement</span></span> | <span data-ttu-id="da1e2-124">值</span><span class="sxs-lookup"><span data-stu-id="da1e2-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="da1e2-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da1e2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="da1e2-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da1e2-126">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="da1e2-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da1e2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="da1e2-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da1e2-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="da1e2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="da1e2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da1e2-130"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da1e2-130"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da1e2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da1e2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da1e2-132">OPM 函式</span><span class="sxs-lookup"><span data-stu-id="da1e2-132">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="da1e2-133">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="da1e2-133">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
