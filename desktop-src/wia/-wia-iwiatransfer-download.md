---
description: 起始將資料下載至呼叫端。
ms.assetid: e639fabb-2c13-4009-affa-1c2b06c0d4c8
title: 'IWiaTransfer：:D 下載 o) 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Download
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 2863915b850588d4db018693d9081ed2907d644a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511632"
---
# <a name="iwiatransferdownload-method"></a><span data-ttu-id="a9c59-103">IWiaTransfer：:D 下載 o) 方法</span><span class="sxs-lookup"><span data-stu-id="a9c59-103">IWiaTransfer::Download method</span></span>

<span data-ttu-id="a9c59-104">起始將資料下載至呼叫端。</span><span class="sxs-lookup"><span data-stu-id="a9c59-104">Initiates a data download to the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c59-105">語法</span><span class="sxs-lookup"><span data-stu-id="a9c59-105">Syntax</span></span>


```C++
HRESULT Download(
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="a9c59-106">參數</span><span class="sxs-lookup"><span data-stu-id="a9c59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9c59-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9c59-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9c59-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="a9c59-108">Type: **LONG**</span></span>

<span data-ttu-id="a9c59-109">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="a9c59-109">Currently unused.</span></span> <span data-ttu-id="a9c59-110">應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="a9c59-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a9c59-111">*pIWiaTransferCallback* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9c59-111">*pIWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9c59-112">類型： \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="a9c59-112">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="a9c59-113">指定呼叫端 [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a9c59-113">Specifies a pointer to the caller's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9c59-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9c59-114">Return value</span></span>

<span data-ttu-id="a9c59-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a9c59-115">Type: **HRESULT**</span></span>

<span data-ttu-id="a9c59-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a9c59-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a9c59-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a9c59-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9c59-118">備註</span><span class="sxs-lookup"><span data-stu-id="a9c59-118">Remarks</span></span>

<span data-ttu-id="a9c59-119">如果資料夾已下載，則該資料夾的所有子專案也會一併傳送。</span><span class="sxs-lookup"><span data-stu-id="a9c59-119">If a folder is downloaded, then all the child items of that folder are also transferred.</span></span> <span data-ttu-id="a9c59-120">每個專案都會在個別的資料流程中傳輸。</span><span class="sxs-lookup"><span data-stu-id="a9c59-120">Each item is transferred in a separate stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9c59-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9c59-121">Requirements</span></span>



| <span data-ttu-id="a9c59-122">需求</span><span class="sxs-lookup"><span data-stu-id="a9c59-122">Requirement</span></span> | <span data-ttu-id="a9c59-123">值</span><span class="sxs-lookup"><span data-stu-id="a9c59-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c59-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9c59-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a9c59-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9c59-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a9c59-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9c59-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a9c59-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9c59-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a9c59-128">標頭</span><span class="sxs-lookup"><span data-stu-id="a9c59-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9c59-129"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="a9c59-129"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="a9c59-130">Idl</span><span class="sxs-lookup"><span data-stu-id="a9c59-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a9c59-131"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a9c59-131"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="a9c59-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="a9c59-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9c59-133"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9c59-133"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




