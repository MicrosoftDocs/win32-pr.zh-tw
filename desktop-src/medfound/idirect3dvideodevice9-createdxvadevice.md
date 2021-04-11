---
description: 建立 (DXVA) 解碼器裝置的 DirectX Video 加速。
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: 'IDirect3DVideoDevice9：： CreateDXVADevice 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateDXVADevice
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 50ce7cee350479f4286921b6cdf69b319033c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114225"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a><span data-ttu-id="d4c19-103">IDirect3DVideoDevice9：： CreateDXVADevice 方法</span><span class="sxs-lookup"><span data-stu-id="d4c19-103">IDirect3DVideoDevice9::CreateDXVADevice method</span></span>

<span data-ttu-id="d4c19-104">建立 (DXVA) 解碼器裝置的 DirectX Video 加速。</span><span class="sxs-lookup"><span data-stu-id="d4c19-104">Creates a DirectX Video Acceleration (DXVA) decoder device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c19-105">語法</span><span class="sxs-lookup"><span data-stu-id="d4c19-105">Syntax</span></span>


```C++
HRESULT CreateDXVADevice(
   GUID                 *pGuid,
   DXVAUncompDataInfo   *pUncompData,
   LPVOID               pData,
   DWORD                DataSize,
   IDirect3DDXVADevice9 **ppDXVADevice
);
```



## <a name="parameters"></a><span data-ttu-id="d4c19-106">參數</span><span class="sxs-lookup"><span data-stu-id="d4c19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4c19-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="d4c19-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="d4c19-108">指定要建立之裝置的 GUID 指標。</span><span class="sxs-lookup"><span data-stu-id="d4c19-108">Pointer to a GUID that specifies the device to create.</span></span>

</dd> <dt>

<span data-ttu-id="d4c19-109">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="d4c19-109">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="d4c19-110">[**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo)結構的指標，指定未壓縮影像的格式。</span><span class="sxs-lookup"><span data-stu-id="d4c19-110">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the format of the uncompressed image.</span></span>

</dd> <dt>

<span data-ttu-id="d4c19-111">*.Pdata*</span><span class="sxs-lookup"><span data-stu-id="d4c19-111">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="d4c19-112">**DXVA \_ ConnectMode** 結構的指標，此結構會指定 DXVA 模式和受限的設定檔。</span><span class="sxs-lookup"><span data-stu-id="d4c19-112">Pointer to a **DXVA\_ConnectMode** structure that specifies the DXVA mode and restricted profile.</span></span>

</dd> <dt>

<span data-ttu-id="d4c19-113">*DataSize*</span><span class="sxs-lookup"><span data-stu-id="d4c19-113">*DataSize*</span></span> 
</dt> <dd>

<span data-ttu-id="d4c19-114">**DXVA \_ ConnectMode** 結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d4c19-114">Size of the **DXVA\_ConnectMode** structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d4c19-115">*ppDXVADevice*</span><span class="sxs-lookup"><span data-stu-id="d4c19-115">*ppDXVADevice*</span></span> 
</dt> <dd>

<span data-ttu-id="d4c19-116">接收 [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d4c19-116">Receives a pointer to the [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) interface.</span></span> <span data-ttu-id="d4c19-117">呼叫端必須釋放介面。</span><span class="sxs-lookup"><span data-stu-id="d4c19-117">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4c19-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4c19-118">Return value</span></span>

<span data-ttu-id="d4c19-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d4c19-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d4c19-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d4c19-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c19-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4c19-121">Requirements</span></span>



| <span data-ttu-id="d4c19-122">需求</span><span class="sxs-lookup"><span data-stu-id="d4c19-122">Requirement</span></span> | <span data-ttu-id="d4c19-123">值</span><span class="sxs-lookup"><span data-stu-id="d4c19-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d4c19-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4c19-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d4c19-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4c19-125">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d4c19-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4c19-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d4c19-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4c19-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d4c19-128">標頭</span><span class="sxs-lookup"><span data-stu-id="d4c19-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4c19-129"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4c19-129"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4c19-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4c19-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c19-131">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="d4c19-131">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




