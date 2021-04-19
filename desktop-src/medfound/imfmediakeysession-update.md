---
description: 針對指定的金鑰系統，傳入內容解密模組所需的任何相關資料的索引鍵值。
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
title: IMFMediaKeySession：： Update 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Update
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 15bc06523f0cf9a7dc433381dd596cea89608ce7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982810"
---
# <a name="imfmediakeysessionupdate-method"></a><span data-ttu-id="7828e-103">IMFMediaKeySession：： Update 方法</span><span class="sxs-lookup"><span data-stu-id="7828e-103">IMFMediaKeySession::Update method</span></span>

<span data-ttu-id="7828e-104">針對指定的金鑰系統，傳入內容解密模組所需的任何相關資料的索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="7828e-104">Passes in a key value with any associated data required by the Content Decryption Module for the given key system.</span></span>

## <a name="syntax"></a><span data-ttu-id="7828e-105">語法</span><span class="sxs-lookup"><span data-stu-id="7828e-105">Syntax</span></span>


```C++
HRESULT Update(
   const BYTE  *key,
         DWORD cb
);
```



## <a name="parameters"></a><span data-ttu-id="7828e-106">參數</span><span class="sxs-lookup"><span data-stu-id="7828e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7828e-107">*key*</span><span class="sxs-lookup"><span data-stu-id="7828e-107">*key*</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="7828e-108">*Cb*</span><span class="sxs-lookup"><span data-stu-id="7828e-108">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="7828e-109">索引 *鍵* 的計數（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7828e-109">The count in bytes of *key*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7828e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7828e-110">Return value</span></span>

<span data-ttu-id="7828e-111">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="7828e-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7828e-112">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7828e-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7828e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7828e-113">Requirements</span></span>



| <span data-ttu-id="7828e-114">需求</span><span class="sxs-lookup"><span data-stu-id="7828e-114">Requirement</span></span> | <span data-ttu-id="7828e-115">值</span><span class="sxs-lookup"><span data-stu-id="7828e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7828e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7828e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7828e-117">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7828e-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7828e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7828e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7828e-119">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7828e-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7828e-120">Idl</span><span class="sxs-lookup"><span data-stu-id="7828e-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7828e-121"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7828e-121"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7828e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7828e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7828e-123">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="7828e-123">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




