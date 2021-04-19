---
description: 將 IMFSourceBuffer 新增至與 IMFMediaSourceExtension 相關聯的緩衝區集合。
ms.assetid: 1ecb7047-4dc9-4657-8a19-12108de299c0
title: IMFMediaSourceExtension：： AddSourceBuffer 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.AddSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: a62a62d8cf11afaa0190ac442f84b00cfe23517b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982798"
---
# <a name="imfmediasourceextensionaddsourcebuffer-method"></a><span data-ttu-id="79869-103">IMFMediaSourceExtension：： AddSourceBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="79869-103">IMFMediaSourceExtension::AddSourceBuffer method</span></span>

<span data-ttu-id="79869-104">將 [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) 新增至與 [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)相關聯的緩衝區集合。</span><span class="sxs-lookup"><span data-stu-id="79869-104">Adds a [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) to the collection of buffers associated with the [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension).</span></span>

## <a name="syntax"></a><span data-ttu-id="79869-105">語法</span><span class="sxs-lookup"><span data-stu-id="79869-105">Syntax</span></span>


```C++
HRESULT AddSourceBuffer(
  [in]  BSTR                  type,
  [in]  IMFSourceBufferNotify *pNotify,
  [out] IMFSourceBuffer       **ppSourceBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="79869-106">參數</span><span class="sxs-lookup"><span data-stu-id="79869-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79869-107">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79869-107">*type* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79869-108">*pNotify* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79869-108">*pNotify* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79869-109">*ppSourceBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="79869-109">*ppSourceBuffer* \[out\]</span></span>
<span data-ttu-id="79869-110"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="79869-110"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="79869-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="79869-111">Return value</span></span>

<span data-ttu-id="79869-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="79869-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="79869-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="79869-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="79869-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="79869-114">Requirements</span></span>



| <span data-ttu-id="79869-115">需求</span><span class="sxs-lookup"><span data-stu-id="79869-115">Requirement</span></span> | <span data-ttu-id="79869-116">值</span><span class="sxs-lookup"><span data-stu-id="79869-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="79869-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79869-117">Minimum supported client</span></span><br/> | <span data-ttu-id="79869-118">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79869-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="79869-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79869-119">Minimum supported server</span></span><br/> | <span data-ttu-id="79869-120">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79869-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="79869-121">Idl</span><span class="sxs-lookup"><span data-stu-id="79869-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79869-122"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="79869-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79869-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79869-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79869-124">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="79869-124">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




