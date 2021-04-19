---
description: 關閉媒體金鑰會話，且必須在金鑰會話發行之前呼叫。
ms.assetid: 97c6b4bd-a973-4475-a325-0373af9b54b1
title: IMFMediaKeySession：： Close 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Close
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 16e6efbe27c411c38dca92d12e05fe9395c4946b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106992229"
---
# <a name="imfmediakeysessionclose-method"></a><span data-ttu-id="872c5-103">IMFMediaKeySession：： Close 方法</span><span class="sxs-lookup"><span data-stu-id="872c5-103">IMFMediaKeySession::Close method</span></span>

<span data-ttu-id="872c5-104">關閉媒體金鑰會話，且必須在金鑰會話發行之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="872c5-104">Closes the media key session and must be called before the key session is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="872c5-105">語法</span><span class="sxs-lookup"><span data-stu-id="872c5-105">Syntax</span></span>


```C++
HRESULT Close();
```



## <a name="parameters"></a><span data-ttu-id="872c5-106">參數</span><span class="sxs-lookup"><span data-stu-id="872c5-106">Parameters</span></span>

<span data-ttu-id="872c5-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="872c5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="872c5-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="872c5-108">Return value</span></span>

<span data-ttu-id="872c5-109">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="872c5-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="872c5-110">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="872c5-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="872c5-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="872c5-111">Requirements</span></span>



| <span data-ttu-id="872c5-112">需求</span><span class="sxs-lookup"><span data-stu-id="872c5-112">Requirement</span></span> | <span data-ttu-id="872c5-113">值</span><span class="sxs-lookup"><span data-stu-id="872c5-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="872c5-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="872c5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="872c5-115">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="872c5-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="872c5-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="872c5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="872c5-117">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="872c5-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="872c5-118">Idl</span><span class="sxs-lookup"><span data-stu-id="872c5-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="872c5-119"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="872c5-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="872c5-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="872c5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="872c5-121">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="872c5-121">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




