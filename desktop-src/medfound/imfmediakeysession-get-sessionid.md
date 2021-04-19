---
description: 取得為此會話建立的唯一會話識別碼。
ms.assetid: 779ebea9-69ff-469a-8ee0-06d570ede6cb
title: IMFMediaKeySession：： get_SessionId 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.get_SessionId
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 7110dbe6c24d1189019fb242621c7e3c01253264
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981929"
---
# <a name="imfmediakeysessionget_sessionid-method"></a><span data-ttu-id="12f7a-103">IMFMediaKeySession：： get \_ SessionId 方法</span><span class="sxs-lookup"><span data-stu-id="12f7a-103">IMFMediaKeySession::get\_SessionId method</span></span>

<span data-ttu-id="12f7a-104">取得為此會話建立的唯一會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="12f7a-104">Gets a unique session id created for this session.</span></span>

## <a name="syntax"></a><span data-ttu-id="12f7a-105">語法</span><span class="sxs-lookup"><span data-stu-id="12f7a-105">Syntax</span></span>


```C++
HRESULT get_SessionId(
   BSTR *sessionId
);
```



## <a name="parameters"></a><span data-ttu-id="12f7a-106">參數</span><span class="sxs-lookup"><span data-stu-id="12f7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12f7a-107">*sessionId*</span><span class="sxs-lookup"><span data-stu-id="12f7a-107">*sessionId*</span></span> 
</dt> <dd>

<span data-ttu-id="12f7a-108">媒體金鑰會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="12f7a-108">The media key session id.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12f7a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="12f7a-109">Return value</span></span>

<span data-ttu-id="12f7a-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="12f7a-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="12f7a-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="12f7a-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="12f7a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="12f7a-112">Requirements</span></span>



| <span data-ttu-id="12f7a-113">需求</span><span class="sxs-lookup"><span data-stu-id="12f7a-113">Requirement</span></span> | <span data-ttu-id="12f7a-114">值</span><span class="sxs-lookup"><span data-stu-id="12f7a-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="12f7a-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12f7a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="12f7a-116">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12f7a-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="12f7a-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12f7a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="12f7a-118">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12f7a-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="12f7a-119">Idl</span><span class="sxs-lookup"><span data-stu-id="12f7a-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12f7a-120"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="12f7a-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12f7a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12f7a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12f7a-122">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="12f7a-122">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




