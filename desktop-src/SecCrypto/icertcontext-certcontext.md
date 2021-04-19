---
description: 設定或抓取憑證的 PCCERT \_ 內容。
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: ICertCoNtext：： CertCoNtext 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 38bd1c704ca709fc1e4b6072bb68c2105dc5db9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993391"
---
# <a name="icertcontextcertcontext-property"></a><span data-ttu-id="e26c2-103">ICertCoNtext：： CertCoNtext 屬性</span><span class="sxs-lookup"><span data-stu-id="e26c2-103">ICertContext::CertContext property</span></span>

<span data-ttu-id="e26c2-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。\]</span><span class="sxs-lookup"><span data-stu-id="e26c2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="e26c2-105">**CertCoNtext** 屬性會設定或抓取憑證的 PCCERT \_ 內容。</span><span class="sxs-lookup"><span data-stu-id="e26c2-105">The **CertContext** property sets or retrieves the PCCERT\_CONTEXT of a certificate.</span></span>

<span data-ttu-id="e26c2-106">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="e26c2-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e26c2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e26c2-107">Syntax</span></span>


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a><span data-ttu-id="e26c2-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="e26c2-108">Property value</span></span>

<span data-ttu-id="e26c2-109">憑證的 PCCERT \_ 內容。</span><span class="sxs-lookup"><span data-stu-id="e26c2-109">The PCCERT\_CONTEXT of the certificate.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e26c2-110">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e26c2-110">Error codes</span></span>

<span data-ttu-id="e26c2-111">如果屬性存取方法 **put \_ CertCoNtext** 並 **讓 \_ CertCoNtext** 成功，則會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e26c2-111">If the property access methods **put\_CertContext** and **get\_CertContext** succeed, they return S\_OK.</span></span>

<span data-ttu-id="e26c2-112">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="e26c2-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e26c2-113">備註</span><span class="sxs-lookup"><span data-stu-id="e26c2-113">Remarks</span></span>

<span data-ttu-id="e26c2-114">您必須呼叫 [**FreeCoNtext**](icertcontext-freecontext.md) 方法或 [**CertFreeCertificateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) 函數來釋放內容。</span><span class="sxs-lookup"><span data-stu-id="e26c2-114">You must call either the [**FreeContext**](icertcontext-freecontext.md) method or the [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) function to free the context.</span></span>

<span data-ttu-id="e26c2-115">如果您設定 **CertCoNtext** 屬性，則會重設整個 [**憑證**](certificate.md) 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="e26c2-115">If you set the **CertContext** property, the state of the entire [**Certificate**](certificate.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="e26c2-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e26c2-116">Requirements</span></span>



| <span data-ttu-id="e26c2-117">需求</span><span class="sxs-lookup"><span data-stu-id="e26c2-117">Requirement</span></span> | <span data-ttu-id="e26c2-118">值</span><span class="sxs-lookup"><span data-stu-id="e26c2-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e26c2-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e26c2-119">Redistributable</span></span><br/> | <span data-ttu-id="e26c2-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e26c2-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e26c2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e26c2-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="e26c2-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e26c2-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e26c2-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e26c2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e26c2-124">**ICertCoNtext**</span><span class="sxs-lookup"><span data-stu-id="e26c2-124">**ICertContext**</span></span>](icertcontext.md)
</dt> </dl>

 

 




