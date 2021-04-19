---
description: 釋放 \_ 透過 CertCoNtext 屬性取得的 PCCERT 內容。
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: ICertCoNtext：： FreeCoNtext 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.FreeContext
- CertContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1f4c216f6e417726e60d5f2e2bd67387a51d352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976127"
---
# <a name="icertcontextfreecontext-method"></a><span data-ttu-id="f4381-103">ICertCoNtext：： FreeCoNtext 方法</span><span class="sxs-lookup"><span data-stu-id="f4381-103">ICertContext::FreeContext method</span></span>

<span data-ttu-id="f4381-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。\]</span><span class="sxs-lookup"><span data-stu-id="f4381-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="f4381-105">**FreeCoNtext** 方法會釋放 \_ 透過 [**CERTCONTEXT**](icertcontext-certcontext.md)屬性取得的 PCCERT 內容。</span><span class="sxs-lookup"><span data-stu-id="f4381-105">The **FreeContext** method releases a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4381-106">語法</span><span class="sxs-lookup"><span data-stu-id="f4381-106">Syntax</span></span>


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a><span data-ttu-id="f4381-107">參數</span><span class="sxs-lookup"><span data-stu-id="f4381-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4381-108">*pCertCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f4381-108">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4381-109">\_要釋放的 PCCERT 內容。</span><span class="sxs-lookup"><span data-stu-id="f4381-109">The PCCERT\_CONTEXT to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4381-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4381-110">Return value</span></span>

<span data-ttu-id="f4381-111">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="f4381-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="f4381-112">S 的值 \_ 表示成功。</span><span class="sxs-lookup"><span data-stu-id="f4381-112">A value of S\_OK indicates success.</span></span> <span data-ttu-id="f4381-113">任何其他值則表示作業失敗。</span><span class="sxs-lookup"><span data-stu-id="f4381-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4381-114">備註</span><span class="sxs-lookup"><span data-stu-id="f4381-114">Remarks</span></span>

<span data-ttu-id="f4381-115">這個方法不會釋放 \_ [**憑證**](certificate.md) 物件中所包含的 PCCERT 內容。</span><span class="sxs-lookup"><span data-stu-id="f4381-115">This method does not release the PCCERT\_CONTEXT contained within a [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="f4381-116">它只能用來釋放 \_ 透過 [**CertCoNtext**](icertcontext-certcontext.md) 屬性取得的 PCCERT 內容。</span><span class="sxs-lookup"><span data-stu-id="f4381-116">It should be used only to release a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4381-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4381-117">Requirements</span></span>



| <span data-ttu-id="f4381-118">需求</span><span class="sxs-lookup"><span data-stu-id="f4381-118">Requirement</span></span> | <span data-ttu-id="f4381-119">值</span><span class="sxs-lookup"><span data-stu-id="f4381-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4381-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f4381-120">Redistributable</span></span><br/> | <span data-ttu-id="f4381-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f4381-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f4381-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f4381-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="f4381-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4381-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4381-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4381-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4381-125">**ICertCoNtext**</span><span class="sxs-lookup"><span data-stu-id="f4381-125">**ICertContext**</span></span>](icertcontext.md)
</dt> </dl>

 

 




