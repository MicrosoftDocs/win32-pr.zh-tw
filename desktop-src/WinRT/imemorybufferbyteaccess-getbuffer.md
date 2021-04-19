---
description: 取得 IMemoryBuffer，表示為位元組陣列。
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: IMemoryBufferByteAccess：： GetBuffer 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMemoryBufferByteAccess.GetBuffer
api_type:
- COM
api_location: ''
ms.openlocfilehash: f31d1506822f21977e2d60492248c2d70a51829c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973276"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a><span data-ttu-id="bfa16-103">IMemoryBufferByteAccess：： GetBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="bfa16-103">IMemoryBufferByteAccess::GetBuffer method</span></span>

<span data-ttu-id="bfa16-104">取得 [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) ，表示為位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="bfa16-104">Gets an [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) as an array of bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa16-105">語法</span><span class="sxs-lookup"><span data-stu-id="bfa16-105">Syntax</span></span>


```C++
HRESULT GetBuffer(
  [out] BYTE   **value,
  [out] UINT32 *capacity
);
```



## <a name="parameters"></a><span data-ttu-id="bfa16-106">參數</span><span class="sxs-lookup"><span data-stu-id="bfa16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa16-107">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bfa16-107">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa16-108">包含緩衝區資料的位元組陣列指標。</span><span class="sxs-lookup"><span data-stu-id="bfa16-108">A pointer to a byte array containing the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="bfa16-109">*容量* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bfa16-109">*capacity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa16-110">傳回陣列中的位元組數目</span><span class="sxs-lookup"><span data-stu-id="bfa16-110">The number of bytes in the returned array</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfa16-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bfa16-111">Return value</span></span>

<span data-ttu-id="bfa16-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="bfa16-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bfa16-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bfa16-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfa16-114">備註</span><span class="sxs-lookup"><span data-stu-id="bfa16-114">Remarks</span></span>

<span data-ttu-id="bfa16-115">呼叫 [**MemoryBuffer：： Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) 時，使用這個緩衝區的程式碼應該將 *值* 指標設為 null。</span><span class="sxs-lookup"><span data-stu-id="bfa16-115">When [**MemoryBuffer::Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) is called, the code using this buffer should set the *value* pointer to null.</span></span>

## <a name="see-also"></a><span data-ttu-id="bfa16-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfa16-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="bfa16-117">[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bfa16-117">[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))</span></span>
</dt> </dl>

 

 
