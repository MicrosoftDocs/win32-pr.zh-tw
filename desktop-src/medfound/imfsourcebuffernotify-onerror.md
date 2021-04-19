---
description: 用來指出來源緩衝區發生錯誤。
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: IMFSourceBufferNotify：： OnError 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBufferNotify.OnError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 8b5f48c3517eb62b0a70acb9cbb28a5ecf7c90cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996617"
---
# <a name="imfsourcebuffernotifyonerror-method"></a><span data-ttu-id="b6cf5-103">IMFSourceBufferNotify：： OnError 方法</span><span class="sxs-lookup"><span data-stu-id="b6cf5-103">IMFSourceBufferNotify::OnError method</span></span>

<span data-ttu-id="b6cf5-104">用來指出來源緩衝區發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b6cf5-104">Used to indicate that an error has occurred with the source buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6cf5-105">語法</span><span class="sxs-lookup"><span data-stu-id="b6cf5-105">Syntax</span></span>


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="b6cf5-106">參數</span><span class="sxs-lookup"><span data-stu-id="b6cf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6cf5-107">*hr* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6cf5-107">*hr* \[in\]</span></span>
<span data-ttu-id="b6cf5-108"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b6cf5-108"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="b6cf5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6cf5-109">Return value</span></span>

<span data-ttu-id="b6cf5-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b6cf5-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6cf5-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6cf5-111">Requirements</span></span>



| <span data-ttu-id="b6cf5-112">需求</span><span class="sxs-lookup"><span data-stu-id="b6cf5-112">Requirement</span></span> | <span data-ttu-id="b6cf5-113">值</span><span class="sxs-lookup"><span data-stu-id="b6cf5-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6cf5-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6cf5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b6cf5-115">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6cf5-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b6cf5-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6cf5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b6cf5-117">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6cf5-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b6cf5-118">Idl</span><span class="sxs-lookup"><span data-stu-id="b6cf5-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6cf5-119"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6cf5-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6cf5-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6cf5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6cf5-121">**IMFSourceBufferNotify**</span><span class="sxs-lookup"><span data-stu-id="b6cf5-121">**IMFSourceBufferNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 




