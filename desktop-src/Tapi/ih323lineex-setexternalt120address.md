---
description: 應用程式會呼叫 SetExternalT120Address 方法來設定資料交換的外部 T. 120 位址。
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: 'IH323LineEx：： SetExternalT120Address 方法 (H323priv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09756aaf77ba36497b3059f7e93829d7d6a57b42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990148"
---
# <a name="ih323lineexsetexternalt120address-method"></a><span data-ttu-id="ff580-103">IH323LineEx：： SetExternalT120Address 方法</span><span class="sxs-lookup"><span data-stu-id="ff580-103">IH323LineEx::SetExternalT120Address method</span></span>

<span data-ttu-id="ff580-104">\[**SetExternalT120Address** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="ff580-104">\[**SetExternalT120Address** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ff580-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="ff580-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ff580-106">應用程式會呼叫 **SetExternalT120Address** 方法來設定資料交換的外部 T. 120 位址。</span><span class="sxs-lookup"><span data-stu-id="ff580-106">The **SetExternalT120Address** method is called by an application to configure an external T.120 address for data exchange.</span></span> <span data-ttu-id="ff580-107">在 h.264 協商期間將會公告 T. 120 功能，而位址將用於 open 邏輯通道通知，讓另一個端點可以設定與接聽該位址的服務有關的 T. 120 個會話。</span><span class="sxs-lookup"><span data-stu-id="ff580-107">T.120 capability will be advertised during the H.245 negotiation, and the address will be used in the open logic channel acknowledgement so that the other endpoint can set up T.120 sessions with the service listening on that address.</span></span> <span data-ttu-id="ff580-108">如果未呼叫此函式，則 h. 服務提供者將不會公告 T. 120 功能。</span><span class="sxs-lookup"><span data-stu-id="ff580-108">If this function is not called, the H.323 service provider will not advertise T.120 capability.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff580-109">語法</span><span class="sxs-lookup"><span data-stu-id="ff580-109">Syntax</span></span>


```C++
HRESULT SetExternalT120Address(
  [in] BOOL  fEnable,
  [in] DWORD dwIP,
  [in] WORD  wPort
);
```



## <a name="parameters"></a><span data-ttu-id="ff580-110">參數</span><span class="sxs-lookup"><span data-stu-id="ff580-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff580-111">*fEnable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff580-111">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff580-112">**TRUE** 表示啟用 T. 120 功能; **FALSE** 表示停用 T. 120 功能。</span><span class="sxs-lookup"><span data-stu-id="ff580-112">**TRUE** to enable T.120 capability; **FALSE** to disable T.120 capability.</span></span>

</dd> <dt>

<span data-ttu-id="ff580-113">*dwIP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff580-113">*dwIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff580-114">**DWORD** ，包含以外部的 T. 120 服務之主機位元組順序的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ff580-114">**DWORD** containing the IP address in host byte order of the external T.120 service.</span></span>

</dd> <dt>

<span data-ttu-id="ff580-115">*wPort* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff580-115">*wPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff580-116">包含外部 T. 120 服務之埠的 **單字**。</span><span class="sxs-lookup"><span data-stu-id="ff580-116">**WORD** containing the port of the external T.120 service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff580-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff580-117">Return value</span></span>

<span data-ttu-id="ff580-118">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ff580-118">This method can return one of these values.</span></span>



| <span data-ttu-id="ff580-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ff580-119">Return code</span></span>                                                                          | <span data-ttu-id="ff580-120">Description</span><span class="sxs-lookup"><span data-stu-id="ff580-120">Description</span></span>                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="ff580-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ff580-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ff580-122">方法成功。</span><span class="sxs-lookup"><span data-stu-id="ff580-122">Method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ff580-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff580-123">Requirements</span></span>



| <span data-ttu-id="ff580-124">需求</span><span class="sxs-lookup"><span data-stu-id="ff580-124">Requirement</span></span> | <span data-ttu-id="ff580-125">值</span><span class="sxs-lookup"><span data-stu-id="ff580-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff580-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="ff580-126">TAPI version</span></span><br/> | <span data-ttu-id="ff580-127">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ff580-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ff580-128">標頭</span><span class="sxs-lookup"><span data-stu-id="ff580-128">Header</span></span><br/>       | <dl> <span data-ttu-id="ff580-129"><dt>H323priv。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff580-129"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="ff580-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="ff580-130">Library</span></span><br/>      | <dl> <span data-ttu-id="ff580-131"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="ff580-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ff580-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ff580-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="ff580-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff580-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




