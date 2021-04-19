---
description: 查詢硬體抽象層 (HAL) 將配置給其私用的記憶體數量。
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: 'IDirect3DVideoDevice9：： GetDXVAInternalInfo 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAInternalInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: aa512130b622d192acc37d8c309f462f8ecc87e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977188"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a><span data-ttu-id="3cf14-103">IDirect3DVideoDevice9：： GetDXVAInternalInfo 方法</span><span class="sxs-lookup"><span data-stu-id="3cf14-103">IDirect3DVideoDevice9::GetDXVAInternalInfo method</span></span>

<span data-ttu-id="3cf14-104">查詢硬體抽象層 (HAL) 將配置給其私用的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="3cf14-104">Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cf14-105">語法</span><span class="sxs-lookup"><span data-stu-id="3cf14-105">Syntax</span></span>


```C++
HRESULT GetDXVAInternalInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pMemoryUsed
);
```



## <a name="parameters"></a><span data-ttu-id="3cf14-106">參數</span><span class="sxs-lookup"><span data-stu-id="3cf14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cf14-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="3cf14-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="3cf14-108">指定 DXVA 設定檔之 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="3cf14-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="3cf14-109">若要取得支援的配置檔案清單，請呼叫 [**IDirect3DVideoDevice9：： GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md)。</span><span class="sxs-lookup"><span data-stu-id="3cf14-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf14-110">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="3cf14-110">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="3cf14-111">[**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo)結構的指標，指定未壓縮資料的大小和像素格式。</span><span class="sxs-lookup"><span data-stu-id="3cf14-111">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the size and pixel format of the uncompressed data.</span></span>

</dd> <dt>

<span data-ttu-id="3cf14-112">*pMemoryUsed*</span><span class="sxs-lookup"><span data-stu-id="3cf14-112">*pMemoryUsed*</span></span> 
</dt> <dd>

<span data-ttu-id="3cf14-113">接收 HAL 將配置的臨時記憶體量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3cf14-113">Receives the amount of scratch memory that the HAL will allocate, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cf14-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3cf14-114">Return value</span></span>

<span data-ttu-id="3cf14-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3cf14-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3cf14-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3cf14-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cf14-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cf14-117">Requirements</span></span>



| <span data-ttu-id="3cf14-118">需求</span><span class="sxs-lookup"><span data-stu-id="3cf14-118">Requirement</span></span> | <span data-ttu-id="3cf14-119">值</span><span class="sxs-lookup"><span data-stu-id="3cf14-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3cf14-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3cf14-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3cf14-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cf14-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3cf14-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3cf14-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3cf14-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cf14-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3cf14-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3cf14-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cf14-125"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="3cf14-125"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cf14-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cf14-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf14-127">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="3cf14-127">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




