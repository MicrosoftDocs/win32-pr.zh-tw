---
description: 抓取憑證的指定屬性。
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: CertStoreProvGetCertProperty 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 50de9a73438e2755e002570f921d15e6086a4b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978920"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a><span data-ttu-id="2f3a1-103">CertStoreProvGetCertProperty 回呼函式</span><span class="sxs-lookup"><span data-stu-id="2f3a1-103">CertStoreProvGetCertProperty callback function</span></span>

<span data-ttu-id="2f3a1-104">**CertStoreProvGetCertProperty** 回呼函式會抓取憑證的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="2f3a1-104">The **CertStoreProvGetCertProperty** callback function retrieves a specified property of a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f3a1-105">語法</span><span class="sxs-lookup"><span data-stu-id="2f3a1-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="2f3a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="2f3a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f3a1-107">*hStoreProv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f3a1-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f3a1-108">**HCERTSTOREPROV** [*憑證存放區*](../secgloss/c-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2f3a1-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f3a1-109">*pCertCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f3a1-109">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f3a1-110">憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2f3a1-110">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2f3a1-111">*dwPropId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f3a1-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f3a1-112">表示屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f3a1-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2f3a1-113">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f3a1-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f3a1-114">任何需要的旗標值。</span><span class="sxs-lookup"><span data-stu-id="2f3a1-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="2f3a1-115">*pvData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2f3a1-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f3a1-116">緩衝區的指標，其中包含要由函式傳回之憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2f3a1-116">A pointer to a buffer to contain the pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure to be returned by the function.</span></span> <span data-ttu-id="2f3a1-117">在第一次呼叫函式時，可以設定為 **Null** ，以取得 *pcbData* 的值，然後再為緩衝區配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="2f3a1-117">May be set to **NULL** on a first call to the function to get the value of *pcbData* before allocating memory for the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2f3a1-118">*pcbData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2f3a1-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f3a1-119">**DWORD** 的指標，表示 *pvData* 緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="2f3a1-119">A pointer to a **DWORD** indicating the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f3a1-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f3a1-120">Return value</span></span>

<span data-ttu-id="2f3a1-121">如果函式成功，則傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="2f3a1-121">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f3a1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f3a1-122">Requirements</span></span>



| <span data-ttu-id="2f3a1-123">需求</span><span class="sxs-lookup"><span data-stu-id="2f3a1-123">Requirement</span></span> | <span data-ttu-id="2f3a1-124">值</span><span class="sxs-lookup"><span data-stu-id="2f3a1-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2f3a1-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f3a1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2f3a1-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f3a1-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2f3a1-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f3a1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2f3a1-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f3a1-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f3a1-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f3a1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f3a1-130">**憑證 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="2f3a1-130">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
