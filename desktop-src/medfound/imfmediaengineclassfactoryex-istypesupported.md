---
description: 取得值，這個值會指出指定的金鑰系統是否支援指定的媒體類型。
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: IMFMediaEngineClassFactoryEx：： IsTypeSupported 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineClassFactoryEx.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 92bf3d64d36c043e9e33b897294ff74a3fda0445
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981923"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a><span data-ttu-id="98e70-103">IMFMediaEngineClassFactoryEx：： IsTypeSupported 方法</span><span class="sxs-lookup"><span data-stu-id="98e70-103">IMFMediaEngineClassFactoryEx::IsTypeSupported method</span></span>

<span data-ttu-id="98e70-104">取得值，這個值會指出指定的金鑰系統是否支援指定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="98e70-104">Gets a value that indicates if the specified key system supports the specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e70-105">語法</span><span class="sxs-lookup"><span data-stu-id="98e70-105">Syntax</span></span>


```C++
HRESULT IsTypeSupported(
   BSTR type,
   BSTR keySystem,
   BOOL *isSupported
);
```



## <a name="parameters"></a><span data-ttu-id="98e70-106">參數</span><span class="sxs-lookup"><span data-stu-id="98e70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e70-107">*type*</span><span class="sxs-lookup"><span data-stu-id="98e70-107">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="98e70-108">要檢查支援的 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="98e70-108">The MIME type to check support for.</span></span>

</dd> <dt>

<span data-ttu-id="98e70-109">*keySystem*</span><span class="sxs-lookup"><span data-stu-id="98e70-109">*keySystem*</span></span> 
</dt> <dd>

<span data-ttu-id="98e70-110">檢查支援的關鍵系統。</span><span class="sxs-lookup"><span data-stu-id="98e70-110">The key system to check support for.</span></span>

</dd> <dt>

<span data-ttu-id="98e70-111">*isSupported*</span><span class="sxs-lookup"><span data-stu-id="98e70-111">*isSupported*</span></span> 
</dt> <dd>

<span data-ttu-id="98e70-112">如果 *keySystem* 支援型別，則 **為 true** ;否則 **為 false。**</span><span class="sxs-lookup"><span data-stu-id="98e70-112">**true** if type is supported by *keySystem*; otherwise, **false.**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98e70-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="98e70-113">Return value</span></span>

<span data-ttu-id="98e70-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="98e70-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="98e70-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="98e70-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="98e70-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="98e70-116">Requirements</span></span>



| <span data-ttu-id="98e70-117">需求</span><span class="sxs-lookup"><span data-stu-id="98e70-117">Requirement</span></span> | <span data-ttu-id="98e70-118">值</span><span class="sxs-lookup"><span data-stu-id="98e70-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="98e70-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98e70-119">Minimum supported client</span></span><br/> | <span data-ttu-id="98e70-120">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98e70-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="98e70-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98e70-121">Minimum supported server</span></span><br/> | <span data-ttu-id="98e70-122">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98e70-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="98e70-123">Idl</span><span class="sxs-lookup"><span data-stu-id="98e70-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="98e70-124"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="98e70-124"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e70-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98e70-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e70-126">**IMFMediaEngineClassFactoryEx**</span><span class="sxs-lookup"><span data-stu-id="98e70-126">**IMFMediaEngineClassFactoryEx**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




