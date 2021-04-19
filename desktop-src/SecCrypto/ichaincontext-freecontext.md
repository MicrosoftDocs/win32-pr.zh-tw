---
description: 釋放 \_ \_ 透過 ChainCoNtext 屬性取得的 PCCERT 鏈內容。
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: IChainCoNtext：： FreeCoNtext 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 413b119f250bfbd061301391fee7741362979f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001834"
---
# <a name="ichaincontextfreecontext-method"></a><span data-ttu-id="1b90d-103">IChainCoNtext：： FreeCoNtext 方法</span><span class="sxs-lookup"><span data-stu-id="1b90d-103">IChainContext::FreeContext method</span></span>

<span data-ttu-id="1b90d-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。\]</span><span class="sxs-lookup"><span data-stu-id="1b90d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="1b90d-105">**FreeCoNtext** 方法會釋放 \_ \_ 透過 [**ChainCoNtext**](ichaincontext-chaincontext.md)屬性取得的 PCCERT 鏈內容。</span><span class="sxs-lookup"><span data-stu-id="1b90d-105">The **FreeContext** method releases a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b90d-106">語法</span><span class="sxs-lookup"><span data-stu-id="1b90d-106">Syntax</span></span>


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a><span data-ttu-id="1b90d-107">參數</span><span class="sxs-lookup"><span data-stu-id="1b90d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b90d-108">*pChainCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1b90d-108">*pChainContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b90d-109">\_要釋放的 PCCERT 鏈 \_ 內容。</span><span class="sxs-lookup"><span data-stu-id="1b90d-109">The PCCERT\_CHAIN\_CONTEXT to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b90d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b90d-110">Return value</span></span>

<span data-ttu-id="1b90d-111">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="1b90d-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="1b90d-112">S 的值 \_ 表示成功。</span><span class="sxs-lookup"><span data-stu-id="1b90d-112">A value of S\_OK indicates success.</span></span> <span data-ttu-id="1b90d-113">任何其他值則表示作業失敗。</span><span class="sxs-lookup"><span data-stu-id="1b90d-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b90d-114">備註</span><span class="sxs-lookup"><span data-stu-id="1b90d-114">Remarks</span></span>

<span data-ttu-id="1b90d-115">這個方法不會釋放 \_ \_ [**連鎖**](chain.md) 物件內所包含的 PCCERT 鏈內容。</span><span class="sxs-lookup"><span data-stu-id="1b90d-115">This method does not release the PCCERT\_CHAIN\_CONTEXT contained within a [**Chain**](chain.md) object.</span></span> <span data-ttu-id="1b90d-116">它只能用來釋放 \_ \_ 透過 [**ChainCoNtext**](ichaincontext-chaincontext.md) 屬性取得的 PCCERT 鏈內容。</span><span class="sxs-lookup"><span data-stu-id="1b90d-116">It should be used only to release a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b90d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b90d-117">Requirements</span></span>



| <span data-ttu-id="1b90d-118">需求</span><span class="sxs-lookup"><span data-stu-id="1b90d-118">Requirement</span></span> | <span data-ttu-id="1b90d-119">值</span><span class="sxs-lookup"><span data-stu-id="1b90d-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b90d-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1b90d-120">Redistributable</span></span><br/> | <span data-ttu-id="1b90d-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1b90d-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1b90d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1b90d-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="1b90d-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b90d-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b90d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b90d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b90d-125">**IChainCoNtext**</span><span class="sxs-lookup"><span data-stu-id="1b90d-125">**IChainContext**</span></span>](ichaincontext.md)
</dt> </dl>

 

 




