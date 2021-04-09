---
description: 建立 IEnumWiaItem2 介面的其他實例，並將指標傳回給它。
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: 'IEnumWiaItem2：： Clone 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Clone
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3279e7db3efe66e940adbcb9677204e5df7867f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691112"
---
# <a name="ienumwiaitem2clone-method"></a><span data-ttu-id="041f3-103">IEnumWiaItem2：： Clone 方法</span><span class="sxs-lookup"><span data-stu-id="041f3-103">IEnumWiaItem2::Clone method</span></span>

<span data-ttu-id="041f3-104">建立 [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) 介面的其他實例，並將指標傳回給它。</span><span class="sxs-lookup"><span data-stu-id="041f3-104">Creates an additional instance of the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface and sends back a pointer to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="041f3-105">語法</span><span class="sxs-lookup"><span data-stu-id="041f3-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="041f3-106">參數</span><span class="sxs-lookup"><span data-stu-id="041f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="041f3-107">*ppIEnum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="041f3-107">*ppIEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="041f3-108">類型： **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="041f3-108">Type: **[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***</span></span>

<span data-ttu-id="041f3-109">接收 **IEnumWiaItem2：： Clone** 建立之 [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)介面實例的位址。</span><span class="sxs-lookup"><span data-stu-id="041f3-109">Receives the address of the [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface instance that **IEnumWiaItem2::Clone** creates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="041f3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="041f3-110">Return value</span></span>

<span data-ttu-id="041f3-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="041f3-111">Type: **HRESULT**</span></span>

<span data-ttu-id="041f3-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="041f3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="041f3-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="041f3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="041f3-114">備註</span><span class="sxs-lookup"><span data-stu-id="041f3-114">Remarks</span></span>

<span data-ttu-id="041f3-115">應用程式必須在透過 *ppIEnum* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="041f3-115">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="041f3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="041f3-116">Requirements</span></span>



| <span data-ttu-id="041f3-117">需求</span><span class="sxs-lookup"><span data-stu-id="041f3-117">Requirement</span></span> | <span data-ttu-id="041f3-118">值</span><span class="sxs-lookup"><span data-stu-id="041f3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="041f3-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="041f3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="041f3-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="041f3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="041f3-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="041f3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="041f3-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="041f3-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="041f3-123">標頭</span><span class="sxs-lookup"><span data-stu-id="041f3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="041f3-124"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="041f3-124"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="041f3-125">Idl</span><span class="sxs-lookup"><span data-stu-id="041f3-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="041f3-126"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="041f3-126"><dt>Wia.idl</dt></span></span> </dl> |



 

 
