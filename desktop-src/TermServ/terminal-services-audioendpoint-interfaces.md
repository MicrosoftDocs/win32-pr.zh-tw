---
title: 遠端桌面服務 AudioEndpoint 介面
description: 下列介面適用于 AudioEndpoint API。
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de520571c99bf84472760e8a1ca28a52a1d6c32e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106978563"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a><span data-ttu-id="e8672-103">遠端桌面服務 AudioEndpoint 介面</span><span class="sxs-lookup"><span data-stu-id="e8672-103">Remote Desktop Services AudioEndpoint Interfaces</span></span>

<span data-ttu-id="e8672-104">下列介面適用于 AudioEndpoint API。</span><span class="sxs-lookup"><span data-stu-id="e8672-104">The following interfaces are used with the AudioEndpoint API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e8672-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="e8672-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="e8672-106">**IAudioDeviceEndpoint**</span><span class="sxs-lookup"><span data-stu-id="e8672-106">**IAudioDeviceEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

<span data-ttu-id="e8672-107">初始化裝置端點物件，並取得其所代表之裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="e8672-107">Initializes a device endpoint object and gets the capabilities of the device that it represents.</span></span>

</dd> <dt>

[<span data-ttu-id="e8672-108">**IAudioEndpoint**</span><span class="sxs-lookup"><span data-stu-id="e8672-108">**IAudioEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

<span data-ttu-id="e8672-109">提供有關音訊端點的音訊引擎資訊。</span><span class="sxs-lookup"><span data-stu-id="e8672-109">Provides information to the audio engine about an audio endpoint.</span></span> <span data-ttu-id="e8672-110">此介面是由音訊端點所執行。</span><span class="sxs-lookup"><span data-stu-id="e8672-110">This interface is implemented by an audio endpoint.</span></span>

</dd> <dt>

[<span data-ttu-id="e8672-111">**IAudioEndpointControl**</span><span class="sxs-lookup"><span data-stu-id="e8672-111">**IAudioEndpointControl**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

<span data-ttu-id="e8672-112">控制端點的資料流程狀態。</span><span class="sxs-lookup"><span data-stu-id="e8672-112">Controls the stream state of an endpoint.</span></span>

</dd> <dt>

[<span data-ttu-id="e8672-113">**IAudioEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="e8672-113">**IAudioEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

<span data-ttu-id="e8672-114">取得端點緩衝區中目前讀取和寫入位置之間的差異。</span><span class="sxs-lookup"><span data-stu-id="e8672-114">Gets the difference between the current read and write positions in the endpoint buffer.</span></span>

</dd> <dt>

[<span data-ttu-id="e8672-115">**IAudioInputEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="e8672-115">**IAudioInputEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

<span data-ttu-id="e8672-116">取得每個處理階段的輸入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e8672-116">Gets the input buffer for each processing pass.</span></span>

</dd> <dt>

[<span data-ttu-id="e8672-117">**IAudioOutputEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="e8672-117">**IAudioOutputEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

<span data-ttu-id="e8672-118">取得每個處理階段的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e8672-118">Gets the output buffer for each processing pass.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8672-119">備註</span><span class="sxs-lookup"><span data-stu-id="e8672-119">Remarks</span></span>

<span data-ttu-id="e8672-120">遠端桌面服務 AudioEndpoint API 適用于遠端桌面案例;它不適用於用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="e8672-120">The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.</span></span>

 

 




