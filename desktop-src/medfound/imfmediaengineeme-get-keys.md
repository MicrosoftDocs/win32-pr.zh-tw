---
description: 取得與媒體引擎相關聯的媒體索引鍵物件，如果沒有媒體索引鍵物件，則為 null。
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: IMFMediaEngineEME：： get_Keys 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineEME.get_Keys
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982149"
---
# <a name="imfmediaengineemeget_keys-method"></a><span data-ttu-id="73e45-103">IMFMediaEngineEME：： get \_ Keys 方法</span><span class="sxs-lookup"><span data-stu-id="73e45-103">IMFMediaEngineEME::get\_Keys method</span></span>

<span data-ttu-id="73e45-104">取得與媒體引擎相關聯的媒體索引鍵物件，如果沒有媒體索引鍵物件，則 **為 null** 。</span><span class="sxs-lookup"><span data-stu-id="73e45-104">Gets the media keys object associated with the media engine or **null** if there is not a media keys object.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e45-105">語法</span><span class="sxs-lookup"><span data-stu-id="73e45-105">Syntax</span></span>


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a><span data-ttu-id="73e45-106">參數</span><span class="sxs-lookup"><span data-stu-id="73e45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73e45-107">*鑰匙*</span><span class="sxs-lookup"><span data-stu-id="73e45-107">*keys*</span></span> 
</dt> <dd>

<span data-ttu-id="73e45-108">與媒體引擎相關聯的媒體索引鍵物件，如果沒有媒體按鍵物件則為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="73e45-108">The media keys object associated with the media engine or **null** if there is not a media keys object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73e45-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="73e45-109">Return value</span></span>

<span data-ttu-id="73e45-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="73e45-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73e45-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="73e45-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="73e45-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="73e45-112">Requirements</span></span>



| <span data-ttu-id="73e45-113">需求</span><span class="sxs-lookup"><span data-stu-id="73e45-113">Requirement</span></span> | <span data-ttu-id="73e45-114">值</span><span class="sxs-lookup"><span data-stu-id="73e45-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e45-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73e45-115">Minimum supported client</span></span><br/> | <span data-ttu-id="73e45-116">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73e45-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="73e45-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73e45-117">Minimum supported server</span></span><br/> | <span data-ttu-id="73e45-118">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73e45-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="73e45-119">Idl</span><span class="sxs-lookup"><span data-stu-id="73e45-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="73e45-120"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="73e45-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73e45-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73e45-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e45-122">**IMFMediaEngineEME**</span><span class="sxs-lookup"><span data-stu-id="73e45-122">**IMFMediaEngineEME**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 




