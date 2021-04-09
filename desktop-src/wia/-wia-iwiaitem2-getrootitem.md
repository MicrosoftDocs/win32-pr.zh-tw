---
description: 取得專案物件樹狀結構的根專案，用來表示 Windows 映像取得 (WIA) 2.0 硬體裝置。
ms.assetid: bc31ad4a-0851-4510-a038-83646ffd5c98
title: 'IWiaItem2：： GetRootItem 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetRootItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c8d4f004cc9c7cabaf4898f5e8c838a0399dc106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690567"
---
# <a name="iwiaitem2getrootitem-method"></a><span data-ttu-id="e9a88-103">IWiaItem2：： GetRootItem 方法</span><span class="sxs-lookup"><span data-stu-id="e9a88-103">IWiaItem2::GetRootItem method</span></span>

<span data-ttu-id="e9a88-104">取得專案物件樹狀結構的根專案，用來表示 Windows 映像取得 (WIA) 2.0 硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="e9a88-104">Gets the root item of a tree of item objects used to represent a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a88-105">語法</span><span class="sxs-lookup"><span data-stu-id="e9a88-105">Syntax</span></span>


```C++
HRESULT GetRootItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="e9a88-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9a88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9a88-107">*ppIWiaItem2* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9a88-107">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a88-108">類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e9a88-108">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="e9a88-109">接收根專案之 [**IWiaItem2**](-wia-iwiaitem2.md) 介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="e9a88-109">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9a88-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9a88-110">Return value</span></span>

<span data-ttu-id="e9a88-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e9a88-111">Type: **HRESULT**</span></span>

<span data-ttu-id="e9a88-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e9a88-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e9a88-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e9a88-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9a88-114">備註</span><span class="sxs-lookup"><span data-stu-id="e9a88-114">Remarks</span></span>

<span data-ttu-id="e9a88-115">針對 WIA 2.0 硬體裝置的物件樹狀結構中的任何 [**IWiaItem2**](-wia-iwiaitem2.md) 物件，應用程式會呼叫這個函式，以抓取根專案的指標。</span><span class="sxs-lookup"><span data-stu-id="e9a88-115">Given any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device, the application retrieves a pointer to the root item by calling this function.</span></span>

<span data-ttu-id="e9a88-116">應用程式必須在透過 *ppIWiaItem2* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="e9a88-116">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9a88-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9a88-117">Requirements</span></span>



| <span data-ttu-id="e9a88-118">需求</span><span class="sxs-lookup"><span data-stu-id="e9a88-118">Requirement</span></span> | <span data-ttu-id="e9a88-119">值</span><span class="sxs-lookup"><span data-stu-id="e9a88-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a88-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9a88-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e9a88-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9a88-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e9a88-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9a88-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e9a88-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9a88-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e9a88-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e9a88-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9a88-125"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="e9a88-125"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9a88-126">Idl</span><span class="sxs-lookup"><span data-stu-id="e9a88-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e9a88-127"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e9a88-127"><dt>Wia.idl</dt></span></span> </dl> |



 

 
