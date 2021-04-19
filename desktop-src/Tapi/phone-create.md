---
description: 傳送 TAPI 電話 \_ 建立訊息，以通知應用程式建立新的電話裝置。
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: 'PHONE_CREATE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92dfaad5d4007279f18890021f5cb39c22c4da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993475"
---
# <a name="phone_create-message"></a><span data-ttu-id="686ed-103">電話 \_ 建立訊息</span><span class="sxs-lookup"><span data-stu-id="686ed-103">PHONE\_CREATE message</span></span>

<span data-ttu-id="686ed-104">傳送 TAPI **電話 \_ 建立** 訊息，以通知應用程式建立新的電話裝置。</span><span class="sxs-lookup"><span data-stu-id="686ed-104">The TAPI **PHONE\_CREATE** message is sent to inform applications of the creation of a new phone device.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="686ed-105">參數</span><span class="sxs-lookup"><span data-stu-id="686ed-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="686ed-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="686ed-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="686ed-107">未使用的。</span><span class="sxs-lookup"><span data-stu-id="686ed-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="686ed-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="686ed-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="686ed-109">未使用的。</span><span class="sxs-lookup"><span data-stu-id="686ed-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="686ed-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="686ed-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="686ed-111">新建立裝置的 *hDeviceID* 。</span><span class="sxs-lookup"><span data-stu-id="686ed-111">The *hDeviceID* of the newly created device.</span></span>

</dd> <dt>

<span data-ttu-id="686ed-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="686ed-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="686ed-113">未使用的。</span><span class="sxs-lookup"><span data-stu-id="686ed-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="686ed-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="686ed-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="686ed-115">未使用的。</span><span class="sxs-lookup"><span data-stu-id="686ed-115">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="686ed-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="686ed-116">Return value</span></span>

<span data-ttu-id="686ed-117">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="686ed-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="686ed-118">備註</span><span class="sxs-lookup"><span data-stu-id="686ed-118">Remarks</span></span>

<span data-ttu-id="686ed-119">協商 API 版本1.3 的應用程式會傳送指定 PHONESTATE 重新初始化的 [**電話 \_ 狀態**](phone-state.md) 消息 \_ ，要求他們關閉 API 的使用方式，並再次呼叫 [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) 以取得新的裝置數目。</span><span class="sxs-lookup"><span data-stu-id="686ed-119">Applications that negotiated API version 1.3 are sent a [**PHONE\_STATE**](phone-state.md) message specifying PHONESTATE\_REINIT, which requires them to shut down their use of the API and call [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) again to obtain the new number of devices.</span></span> <span data-ttu-id="686ed-120">不過，在允許重新初始化應用程式之前，TAPI 1.4 版和更新版本不需要關閉所有應用程式。建立新裝置時，可以立即進行重新初始化。</span><span class="sxs-lookup"><span data-stu-id="686ed-120">However, TAPI version 1.4 and above do not require all applications to shut down before allowing applications to reinitialize; reinitialization can take place immediately when a new device is created.</span></span>

<span data-ttu-id="686ed-121">支援 TAPI 1.4 版或更新版本的應用程式會傳送 **電話 \_ 建立** 訊息。</span><span class="sxs-lookup"><span data-stu-id="686ed-121">Applications supporting TAPI version 1.4 or later are sent a **PHONE\_CREATE** message.</span></span> <span data-ttu-id="686ed-122">這會通知他們有新裝置和其新的裝置識別碼存在。</span><span class="sxs-lookup"><span data-stu-id="686ed-122">This informs them of the existence of the new device and its new device identifier.</span></span> <span data-ttu-id="686ed-123">然後，應用程式可以選擇是否嘗試在新裝置的休閒中使用。</span><span class="sxs-lookup"><span data-stu-id="686ed-123">The application can then choose whether or not to attempt working with the new device at its leisure.</span></span>

## <a name="requirements"></a><span data-ttu-id="686ed-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="686ed-124">Requirements</span></span>



| <span data-ttu-id="686ed-125">需求</span><span class="sxs-lookup"><span data-stu-id="686ed-125">Requirement</span></span> | <span data-ttu-id="686ed-126">值</span><span class="sxs-lookup"><span data-stu-id="686ed-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="686ed-127">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="686ed-127">TAPI version</span></span><br/> | <span data-ttu-id="686ed-128">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="686ed-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="686ed-129">標頭</span><span class="sxs-lookup"><span data-stu-id="686ed-129">Header</span></span><br/>       | <dl> <span data-ttu-id="686ed-130"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="686ed-130"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="686ed-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="686ed-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="686ed-132">**電話 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="686ed-132">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="686ed-133">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="686ed-133">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="686ed-134">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="686ed-134">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




