---
description: 抓取 CRL 的指定屬性。
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: CertStoreProvGetCRLProperty 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: bcf69653f03ccfbb52c8247c9ea459000db55e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979104"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a><span data-ttu-id="82f7b-103">CertStoreProvGetCRLProperty 回呼函式</span><span class="sxs-lookup"><span data-stu-id="82f7b-103">CertStoreProvGetCRLProperty callback function</span></span>

<span data-ttu-id="82f7b-104">**CertStoreProvGetCRLProperty** 回呼函式會捕獲指定的 [*CRL*](../secgloss/c-gly.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="82f7b-104">The **CertStoreProvGetCRLProperty** callback function retrieves a specified property of a [*CRL*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="82f7b-105">語法</span><span class="sxs-lookup"><span data-stu-id="82f7b-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="82f7b-106">參數</span><span class="sxs-lookup"><span data-stu-id="82f7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82f7b-107">*hStoreProv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82f7b-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f7b-108">**HCERTSTOREPROV** [*憑證存放區*](../secgloss/c-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="82f7b-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="82f7b-109">*pCrlCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82f7b-109">*pCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f7b-110">[**CRL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="82f7b-110">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="82f7b-111">*dwPropId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82f7b-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f7b-112">表示屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="82f7b-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="82f7b-113">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82f7b-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f7b-114">任何需要的旗標值。</span><span class="sxs-lookup"><span data-stu-id="82f7b-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="82f7b-115">*pvData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="82f7b-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82f7b-116">緩衝區的指標，其中包含要由函式傳回的 [**CRL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="82f7b-116">A pointer to a buffer to contain the pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure to be returned by the function.</span></span> <span data-ttu-id="82f7b-117">在第一次呼叫函式時，可以設定為 **Null** ，以取得 *pcbData* 的值，然後再為緩衝區配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="82f7b-117">May be set to **NULL** on a first call to the function to get the value of *pcbData* before allocating memory for the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="82f7b-118">*pcbData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="82f7b-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="82f7b-119">**DWORD** 的指標，表示 *pvData* 緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="82f7b-119">A pointer to a **DWORD** indicating the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82f7b-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="82f7b-120">Return value</span></span>

<span data-ttu-id="82f7b-121">如果函式成功，則傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="82f7b-121">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="82f7b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="82f7b-122">Requirements</span></span>



| <span data-ttu-id="82f7b-123">需求</span><span class="sxs-lookup"><span data-stu-id="82f7b-123">Requirement</span></span> | <span data-ttu-id="82f7b-124">值</span><span class="sxs-lookup"><span data-stu-id="82f7b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="82f7b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82f7b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="82f7b-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82f7b-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="82f7b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82f7b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="82f7b-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82f7b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82f7b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82f7b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82f7b-130">**CRL \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="82f7b-130">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
