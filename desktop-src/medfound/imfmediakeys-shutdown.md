---
description: 深入瞭解： IMFMediaKeys：： Shutdown 方法
ms.assetid: 464b598c-5fa7-40af-83ba-8619fbd84b04
title: IMFMediaKeys：： Shutdown 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.Shutdown
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9fcee861b53aaf0c9fda2c6265f50fcee60f674c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321603"
---
# <a name="imfmediakeysshutdown-method"></a><span data-ttu-id="f997a-103">IMFMediaKeys：： Shutdown 方法</span><span class="sxs-lookup"><span data-stu-id="f997a-103">IMFMediaKeys::Shutdown method</span></span>

## <a name="syntax"></a><span data-ttu-id="f997a-104">語法</span><span class="sxs-lookup"><span data-stu-id="f997a-104">Syntax</span></span>


```C++
HRESULT Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="f997a-105">參數</span><span class="sxs-lookup"><span data-stu-id="f997a-105">Parameters</span></span>

<span data-ttu-id="f997a-106">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f997a-106">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f997a-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="f997a-107">Return value</span></span>

<span data-ttu-id="f997a-108">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f997a-108">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f997a-109">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f997a-109">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f997a-110">備註</span><span class="sxs-lookup"><span data-stu-id="f997a-110">Remarks</span></span>

<span data-ttu-id="f997a-111">最終發行之前，應用程式應該呼叫 **關機**。</span><span class="sxs-lookup"><span data-stu-id="f997a-111">**Shutdown** should be called by the application before final release.</span></span> <span data-ttu-id="f997a-112">內容解密模組 (CDM) 參考，而任何其他資源則會在此時釋放。</span><span class="sxs-lookup"><span data-stu-id="f997a-112">The Content Decryption Module (CDM) reference and any other resources is released at this point.</span></span> <span data-ttu-id="f997a-113">但是，不會釋放或關閉相關會話。</span><span class="sxs-lookup"><span data-stu-id="f997a-113">However, related sessions are not freed or closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f997a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f997a-114">Requirements</span></span>



| <span data-ttu-id="f997a-115">需求</span><span class="sxs-lookup"><span data-stu-id="f997a-115">Requirement</span></span> | <span data-ttu-id="f997a-116">值</span><span class="sxs-lookup"><span data-stu-id="f997a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f997a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f997a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f997a-118">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f997a-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f997a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f997a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f997a-120">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f997a-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f997a-121">Idl</span><span class="sxs-lookup"><span data-stu-id="f997a-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f997a-122"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f997a-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f997a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f997a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f997a-124">**IMFMediaKeys**</span><span class="sxs-lookup"><span data-stu-id="f997a-124">**IMFMediaKeys**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




