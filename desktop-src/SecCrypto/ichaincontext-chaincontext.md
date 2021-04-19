---
description: 設定或抓取憑證的 PCCERT \_ 鏈 \_ 內容。
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: IChainCoNtext：： ChainCoNtext 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36b2f6f5811c844e4e43544f5b56b8de66cb3bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985970"
---
# <a name="ichaincontextchaincontext-property"></a><span data-ttu-id="eec00-103">IChainCoNtext：： ChainCoNtext 屬性</span><span class="sxs-lookup"><span data-stu-id="eec00-103">IChainContext::ChainContext property</span></span>

<span data-ttu-id="eec00-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。\]</span><span class="sxs-lookup"><span data-stu-id="eec00-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="eec00-105">**ChainCoNtext** 屬性會設定或抓取憑證的 PCCERT \_ 鏈 \_ 內容。</span><span class="sxs-lookup"><span data-stu-id="eec00-105">The **ChainContext** property sets or retrieves the PCCERT\_CHAIN\_CONTEXT of a certificate.</span></span>

<span data-ttu-id="eec00-106">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="eec00-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec00-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eec00-107">Syntax</span></span>


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a><span data-ttu-id="eec00-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="eec00-108">Property value</span></span>

<span data-ttu-id="eec00-109">憑證的 PCCERT \_ 鏈 \_ 內容。</span><span class="sxs-lookup"><span data-stu-id="eec00-109">The PCCERT\_CHAIN\_CONTEXT of the certificate.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eec00-110">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="eec00-110">Error codes</span></span>

<span data-ttu-id="eec00-111">如果屬性存取方法 **put \_ ChainCoNtext** 並 **讓 \_ ChainCoNtext** 成功，則會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="eec00-111">If the property access methods **put\_ChainContext** and **get\_ChainContext** succeed, they return S\_OK.</span></span>

<span data-ttu-id="eec00-112">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="eec00-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="eec00-113">備註</span><span class="sxs-lookup"><span data-stu-id="eec00-113">Remarks</span></span>

<span data-ttu-id="eec00-114">您必須呼叫 [**FreeCoNtext**](ichaincontext-freecontext.md) 方法或 [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) 函數來釋放內容。</span><span class="sxs-lookup"><span data-stu-id="eec00-114">You must call either the [**FreeContext**](ichaincontext-freecontext.md) method or the [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) function to free the context.</span></span>

<span data-ttu-id="eec00-115">如果您設定 **ChainCoNtext** 屬性，則會重設整個 [**鏈**](chain.md) 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="eec00-115">If you set the **ChainContext** property, the state of the entire [**Chain**](chain.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="eec00-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="eec00-116">Requirements</span></span>



| <span data-ttu-id="eec00-117">需求</span><span class="sxs-lookup"><span data-stu-id="eec00-117">Requirement</span></span> | <span data-ttu-id="eec00-118">值</span><span class="sxs-lookup"><span data-stu-id="eec00-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eec00-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="eec00-119">Redistributable</span></span><br/> | <span data-ttu-id="eec00-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="eec00-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="eec00-121">DLL</span><span class="sxs-lookup"><span data-stu-id="eec00-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="eec00-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eec00-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eec00-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eec00-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec00-124">**IChainCoNtext**</span><span class="sxs-lookup"><span data-stu-id="eec00-124">**IChainContext**</span></span>](ichaincontext.md)
</dt> </dl>

 

 




