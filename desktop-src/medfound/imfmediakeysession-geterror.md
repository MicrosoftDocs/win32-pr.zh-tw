---
description: 取得與媒體金鑰會話相關聯的錯誤狀態。
ms.assetid: 4693b7d5-59ee-472f-83fc-1ecbcc165dac
title: IMFMediaKeySession：： GetError 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.GetError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4f0a42601698a9cd62dc6cb23ca9e69ac2cc8a49
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986021"
---
# <a name="imfmediakeysessiongeterror-method"></a><span data-ttu-id="61f61-103">IMFMediaKeySession：： GetError 方法</span><span class="sxs-lookup"><span data-stu-id="61f61-103">IMFMediaKeySession::GetError method</span></span>

<span data-ttu-id="61f61-104">取得與媒體金鑰會話相關聯的錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="61f61-104">Gets the error state associated with the media key session.</span></span>

## <a name="syntax"></a><span data-ttu-id="61f61-105">語法</span><span class="sxs-lookup"><span data-stu-id="61f61-105">Syntax</span></span>


```C++
HRESULT GetError(
   USHORT *code,
   DWORD  *systemCode
);
```



## <a name="parameters"></a><span data-ttu-id="61f61-106">參數</span><span class="sxs-lookup"><span data-stu-id="61f61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61f61-107">*code*</span><span class="sxs-lookup"><span data-stu-id="61f61-107">*code*</span></span> 
</dt> <dd>

<span data-ttu-id="61f61-108">錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="61f61-108">The error code.</span></span>

</dd> <dt>

<span data-ttu-id="61f61-109">*systemCode*</span><span class="sxs-lookup"><span data-stu-id="61f61-109">*systemCode*</span></span> 
</dt> <dd>

<span data-ttu-id="61f61-110">平臺特定錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="61f61-110">Platform specific error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61f61-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="61f61-111">Return value</span></span>

<span data-ttu-id="61f61-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="61f61-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="61f61-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="61f61-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="61f61-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="61f61-114">Requirements</span></span>



| <span data-ttu-id="61f61-115">需求</span><span class="sxs-lookup"><span data-stu-id="61f61-115">Requirement</span></span> | <span data-ttu-id="61f61-116">值</span><span class="sxs-lookup"><span data-stu-id="61f61-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="61f61-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61f61-117">Minimum supported client</span></span><br/> | <span data-ttu-id="61f61-118">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61f61-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="61f61-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61f61-119">Minimum supported server</span></span><br/> | <span data-ttu-id="61f61-120">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61f61-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="61f61-121">Idl</span><span class="sxs-lookup"><span data-stu-id="61f61-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61f61-122"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="61f61-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61f61-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61f61-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61f61-124">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="61f61-124">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




