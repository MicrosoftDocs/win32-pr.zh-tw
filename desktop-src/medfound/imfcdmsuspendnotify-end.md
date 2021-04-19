---
description: 實際的暫止即將發生，不會再對內容解密模組進行任何呼叫， (CDM) 。
ms.assetid: 7a319fbb-9757-45da-8a8b-51dd48f08464
title: IMFCdmSuspendNotify：： End 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.End
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 71843b53fa85fded646fe71f2caa463a71c9415f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981533"
---
# <a name="imfcdmsuspendnotifyend-method"></a><span data-ttu-id="f0e91-103">IMFCdmSuspendNotify：： End 方法</span><span class="sxs-lookup"><span data-stu-id="f0e91-103">IMFCdmSuspendNotify::End method</span></span>

<span data-ttu-id="f0e91-104">實際的暫止即將發生，不會再對內容解密模組進行任何呼叫， (CDM) 。</span><span class="sxs-lookup"><span data-stu-id="f0e91-104">The actual suspend is about to occur and no more calls will be made into the Content Decryption Module (CDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0e91-105">語法</span><span class="sxs-lookup"><span data-stu-id="f0e91-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="f0e91-106">參數</span><span class="sxs-lookup"><span data-stu-id="f0e91-106">Parameters</span></span>

<span data-ttu-id="f0e91-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f0e91-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0e91-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0e91-108">Return value</span></span>

<span data-ttu-id="f0e91-109">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f0e91-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f0e91-110">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f0e91-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e91-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0e91-111">Requirements</span></span>



| <span data-ttu-id="f0e91-112">需求</span><span class="sxs-lookup"><span data-stu-id="f0e91-112">Requirement</span></span> | <span data-ttu-id="f0e91-113">值</span><span class="sxs-lookup"><span data-stu-id="f0e91-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e91-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0e91-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f0e91-115">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0e91-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f0e91-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0e91-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f0e91-117">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0e91-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f0e91-118">Idl</span><span class="sxs-lookup"><span data-stu-id="f0e91-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f0e91-119"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f0e91-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0e91-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0e91-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0e91-121">**IMFCdmSuspendNotify**</span><span class="sxs-lookup"><span data-stu-id="f0e91-121">**IMFCdmSuspendNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




