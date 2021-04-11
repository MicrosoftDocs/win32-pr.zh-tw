---
description: IWiaItem2：： EnumRegisterEventInfo 方法會建立一個列舉值，您可以使用它來取得已註冊應用程式之事件的相關資訊。
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: 'IWiaItem2：： EnumRegisterEventInfo 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumRegisterEventInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b5899b629267f74724129aeae3f66801953d8cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113312"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a><span data-ttu-id="2f803-103">IWiaItem2：： EnumRegisterEventInfo 方法</span><span class="sxs-lookup"><span data-stu-id="2f803-103">IWiaItem2::EnumRegisterEventInfo method</span></span>

<span data-ttu-id="2f803-104">**IWiaItem2：： EnumRegisterEventInfo** 方法會建立一個列舉值，您可以使用它來取得已註冊應用程式之事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f803-104">The **IWiaItem2::EnumRegisterEventInfo** method creates an enumerator that you can use to obtain information about events for which an application is registered.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f803-105">語法</span><span class="sxs-lookup"><span data-stu-id="2f803-105">Syntax</span></span>


```C++
HRESULT EnumRegisterEventInfo(
  [in]        LONG              lFlags,
  [in]  const GUID              *pEventGUID,
  [out]       IEnumWIA_DEV_CAPS **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="2f803-106">參數</span><span class="sxs-lookup"><span data-stu-id="2f803-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f803-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f803-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f803-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="2f803-108">Type: **LONG**</span></span>

<span data-ttu-id="2f803-109">未使用。</span><span class="sxs-lookup"><span data-stu-id="2f803-109">Not used.</span></span> <span data-ttu-id="2f803-110">設定為0。</span><span class="sxs-lookup"><span data-stu-id="2f803-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="2f803-111">*pEventGUID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f803-111">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f803-112">類型： \**CONST GUID \** _</span><span class="sxs-lookup"><span data-stu-id="2f803-112">Type: \**const GUID\** _</span></span>

<span data-ttu-id="2f803-113">識別碼的指標，指定您要取得註冊資訊的硬體事件。</span><span class="sxs-lookup"><span data-stu-id="2f803-113">Pointer to an identifier that specifies the hardware event for which you want to obtain registration information.</span></span>

</dd> <dt>

<span data-ttu-id="2f803-114">_ppIEnum \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2f803-114">_ppIEnum\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f803-115">類型： **[ **IEnumWIA \_ DEV \_ cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span><span class="sxs-lookup"><span data-stu-id="2f803-115">Type: **[**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span></span>

<span data-ttu-id="2f803-116">[**IEnumWIA \_ DEV \_ CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="2f803-116">The address of a pointer to the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f803-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f803-117">Return value</span></span>

<span data-ttu-id="2f803-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2f803-118">Type: **HRESULT**</span></span>

<span data-ttu-id="2f803-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="2f803-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2f803-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2f803-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f803-121">備註</span><span class="sxs-lookup"><span data-stu-id="2f803-121">Remarks</span></span>

<span data-ttu-id="2f803-122">應用程式會呼叫這個方法來建立事件資訊的列舉值物件。</span><span class="sxs-lookup"><span data-stu-id="2f803-122">An application calls this method to create an enumerator object for the event information.</span></span> <span data-ttu-id="2f803-123">**IWiaItem2：： EnumRegisterEventInfo** 會在 *ppIEnum* 參數中儲存列舉值物件的 [**IEnumWIA \_ DEV \_ cap**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)介面位址。</span><span class="sxs-lookup"><span data-stu-id="2f803-123">**IWiaItem2::EnumRegisterEventInfo** stores the address of the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface of the enumerator object in the *ppIEnum* parameter.</span></span> <span data-ttu-id="2f803-124">然後，程式會使用介面指標來列舉所註冊之事件的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f803-124">The program then uses the interface pointer to enumerate the properties of the event for which it is registered.</span></span>

<span data-ttu-id="2f803-125">應用程式必須在透過 *ppIEnum* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="2f803-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers that they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f803-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f803-126">Requirements</span></span>



| <span data-ttu-id="2f803-127">需求</span><span class="sxs-lookup"><span data-stu-id="2f803-127">Requirement</span></span> | <span data-ttu-id="2f803-128">值</span><span class="sxs-lookup"><span data-stu-id="2f803-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2f803-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f803-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2f803-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f803-130">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2f803-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f803-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2f803-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f803-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2f803-133">標頭</span><span class="sxs-lookup"><span data-stu-id="2f803-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f803-134"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="2f803-134"><dt>Wia.h</dt></span></span> </dl> |



 

 
