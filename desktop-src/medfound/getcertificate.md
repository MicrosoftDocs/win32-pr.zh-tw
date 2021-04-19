---
description: 取得顯示驅動程式的憑證。
ms.assetid: eceaf151-1dae-4ff0-9139-7f1789f6c682
title: GetCertificate 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificate
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 30cb17345177b552e51120afd00758a3f6886584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973189"
---
# <a name="getcertificate-function"></a><span data-ttu-id="4710f-103">GetCertificate 函式</span><span class="sxs-lookup"><span data-stu-id="4710f-103">GetCertificate function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4710f-104">[輸出保護管理員](output-protection-manager.md)會使用此函式 (OPM) 來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="4710f-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="4710f-105">應用程式不應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="4710f-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="4710f-106">取得顯示驅動程式的憑證。</span><span class="sxs-lookup"><span data-stu-id="4710f-106">Gets a certificate for a display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="4710f-107">語法</span><span class="sxs-lookup"><span data-stu-id="4710f-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCertificate(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ BYTE                     *pbCertificate,
  _Out_ ULONG                    ulCertificateLength
);
```



## <a name="parameters"></a><span data-ttu-id="4710f-108">參數</span><span class="sxs-lookup"><span data-stu-id="4710f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4710f-109">*pstrDeviceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4710f-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4710f-110">[**UNICODE \_ 字串**](/windows/win32/api/subauth/ns-subauth-unicode_string)結構的指標，其中包含 [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa)函式所傳回之顯示裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="4710f-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="4710f-111">*ctPVPCertificateType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4710f-111">*ctPVPCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4710f-112">憑證的類型，指定為 **DXGKMDT \_ 憑證 \_ 類型** 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="4710f-112">The type of certificate, specified as a member of the **DXGKMDT\_CERTIFICATE\_TYPE** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="4710f-113">*pbCertificate* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4710f-113">*pbCertificate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4710f-114">接收憑證之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="4710f-114">A pointer to a buffer that receives the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="4710f-115">*ulCertificateLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4710f-115">*ulCertificateLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4710f-116">*PbCertificate* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4710f-116">The size of the *pbCertificate* buffer, in bytes.</span></span> <span data-ttu-id="4710f-117">若要取得憑證的大小，請呼叫 [**GetCertificateSize**](getcertificatesize.md)。</span><span class="sxs-lookup"><span data-stu-id="4710f-117">To get the size of the certificate, call [**GetCertificateSize**](getcertificatesize.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4710f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="4710f-118">Return value</span></span>

<span data-ttu-id="4710f-119">如果方法成功，則會傳回 **狀態 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="4710f-119">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="4710f-120">否則，它會傳回一個 **NTSTATUS** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4710f-120">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4710f-121">備註</span><span class="sxs-lookup"><span data-stu-id="4710f-121">Remarks</span></span>

<span data-ttu-id="4710f-122">應用程式應該呼叫 [**IOPMVideoOutput：： StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) 方法，而不是此函數。</span><span class="sxs-lookup"><span data-stu-id="4710f-122">Applications should call the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method instead of this function.</span></span>

<span data-ttu-id="4710f-123">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="4710f-123">This function has no associated import library.</span></span> <span data-ttu-id="4710f-124">若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。</span><span class="sxs-lookup"><span data-stu-id="4710f-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="4710f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="4710f-125">Requirements</span></span>



| <span data-ttu-id="4710f-126">需求</span><span class="sxs-lookup"><span data-stu-id="4710f-126">Requirement</span></span> | <span data-ttu-id="4710f-127">值</span><span class="sxs-lookup"><span data-stu-id="4710f-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4710f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4710f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4710f-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4710f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4710f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4710f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4710f-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4710f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4710f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4710f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4710f-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4710f-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4710f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4710f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4710f-135">OPM 函式</span><span class="sxs-lookup"><span data-stu-id="4710f-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="4710f-136">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="4710f-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
