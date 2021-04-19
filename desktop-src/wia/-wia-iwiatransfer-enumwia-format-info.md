---
description: 針對 Windows 映像取得 (WIA) 2.0 裝置支援的傳輸格式建立枚舉器。
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: 'IWiaTransfer：： EnumWIA_FORMAT_INFO 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.EnumWIA_FORMAT_INFO
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 66f3c91d6023655daf85b2a0d726d98a685b001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972234"
---
# <a name="iwiatransferenumwia_format_info-method"></a><span data-ttu-id="ab6c1-103">IWiaTransfer：： EnumWIA \_ 格式 \_ 資訊方法</span><span class="sxs-lookup"><span data-stu-id="ab6c1-103">IWiaTransfer::EnumWIA\_FORMAT\_INFO method</span></span>

<span data-ttu-id="ab6c1-104">針對 Windows 映像取得 (WIA) 2.0 裝置支援的傳輸格式建立枚舉器。</span><span class="sxs-lookup"><span data-stu-id="ab6c1-104">Creates an enumerator for the transfer formats that the Windows Image Acquisition (WIA) 2.0 device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab6c1-105">語法</span><span class="sxs-lookup"><span data-stu-id="ab6c1-105">Syntax</span></span>


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="ab6c1-106">參數</span><span class="sxs-lookup"><span data-stu-id="ab6c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab6c1-107">*ppIEnum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ab6c1-107">*ppIEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab6c1-108">類型： **[ **IEnumWIA \_ 格式 \_ 資訊**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***</span><span class="sxs-lookup"><span data-stu-id="ab6c1-108">Type: **[**IEnumWIA\_FORMAT\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***</span></span>

<span data-ttu-id="ab6c1-109">列舉值的 [**IEnumWIA \_ 格式 \_ 資訊**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) 介面之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="ab6c1-109">The address of the pointer to the [**IEnumWIA\_FORMAT\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) interface for the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab6c1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab6c1-110">Return value</span></span>

<span data-ttu-id="ab6c1-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ab6c1-111">Type: **HRESULT**</span></span>

<span data-ttu-id="ab6c1-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ab6c1-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab6c1-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ab6c1-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab6c1-114">備註</span><span class="sxs-lookup"><span data-stu-id="ab6c1-114">Remarks</span></span>

<span data-ttu-id="ab6c1-115">應用程式必須在透過 *ppIEnum* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="ab6c1-115">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointer received through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab6c1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab6c1-116">Requirements</span></span>



| <span data-ttu-id="ab6c1-117">需求</span><span class="sxs-lookup"><span data-stu-id="ab6c1-117">Requirement</span></span> | <span data-ttu-id="ab6c1-118">值</span><span class="sxs-lookup"><span data-stu-id="ab6c1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6c1-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab6c1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab6c1-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab6c1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ab6c1-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab6c1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab6c1-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab6c1-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ab6c1-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ab6c1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab6c1-124"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="ab6c1-124"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="ab6c1-125">Idl</span><span class="sxs-lookup"><span data-stu-id="ab6c1-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab6c1-126"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab6c1-126"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="ab6c1-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="ab6c1-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="ab6c1-128"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab6c1-128"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
