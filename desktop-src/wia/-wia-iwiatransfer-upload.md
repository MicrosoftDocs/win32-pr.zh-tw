---
description: 從呼叫端起始單一專案的資料上傳。
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'IWiaTransfer：： Upload 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Upload
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6aae6ca8f86d07ec052fdd59d24b0da2b96599d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191396"
---
# <a name="iwiatransferupload-method"></a><span data-ttu-id="c2be8-103">IWiaTransfer：： Upload 方法</span><span class="sxs-lookup"><span data-stu-id="c2be8-103">IWiaTransfer::Upload method</span></span>

<span data-ttu-id="c2be8-104">從呼叫端起始單一專案的資料上傳。</span><span class="sxs-lookup"><span data-stu-id="c2be8-104">Initiates a data upload of a single item from the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2be8-105">語法</span><span class="sxs-lookup"><span data-stu-id="c2be8-105">Syntax</span></span>


```C++
HRESULT Upload(
  [in] LONG                 lFlags,
  [in] IStream              *pSource,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="c2be8-106">參數</span><span class="sxs-lookup"><span data-stu-id="c2be8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2be8-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2be8-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2be8-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="c2be8-108">Type: **LONG**</span></span>

<span data-ttu-id="c2be8-109">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="c2be8-109">Currently unused.</span></span> <span data-ttu-id="c2be8-110">應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="c2be8-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c2be8-111">*pSource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2be8-111">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2be8-112">類型： \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="c2be8-112">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="c2be8-113">指定 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 資料的指標。</span><span class="sxs-lookup"><span data-stu-id="c2be8-113">Specifies a pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) data.</span></span>

</dd> <dt>

<span data-ttu-id="c2be8-114">_pIWiaTransferCallback \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2be8-114">_pIWiaTransferCallback\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2be8-115">類型： \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="c2be8-115">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="c2be8-116">指定呼叫端 [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c2be8-116">Specifies a pointer to the caller's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2be8-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2be8-117">Return value</span></span>

<span data-ttu-id="c2be8-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c2be8-118">Type: **HRESULT**</span></span>

<span data-ttu-id="c2be8-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c2be8-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c2be8-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c2be8-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2be8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2be8-121">Requirements</span></span>



| <span data-ttu-id="c2be8-122">需求</span><span class="sxs-lookup"><span data-stu-id="c2be8-122">Requirement</span></span> | <span data-ttu-id="c2be8-123">值</span><span class="sxs-lookup"><span data-stu-id="c2be8-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2be8-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2be8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c2be8-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2be8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c2be8-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2be8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c2be8-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2be8-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c2be8-128">標頭</span><span class="sxs-lookup"><span data-stu-id="c2be8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2be8-129"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="c2be8-129"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="c2be8-130">Idl</span><span class="sxs-lookup"><span data-stu-id="c2be8-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c2be8-131"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c2be8-131"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="c2be8-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="c2be8-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2be8-133"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2be8-133"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
