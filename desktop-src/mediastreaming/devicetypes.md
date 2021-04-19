---
title: DeviceTypes 列舉
description: 描述媒體串流 API 所支援的 DLNA 裝置類型。
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- DeviceTypes 列舉媒體串流 API
topic_type:
- apiref
api_name:
- DeviceTypes
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9caf60fa5736f9db442da5787746a49f71c61c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981868"
---
# <a name="devicetypes-enumeration"></a><span data-ttu-id="a5574-104">DeviceTypes 列舉</span><span class="sxs-lookup"><span data-stu-id="a5574-104">DeviceTypes enumeration</span></span>

<span data-ttu-id="a5574-105">描述媒體串流 API 所支援的 DLNA 裝置類型。</span><span class="sxs-lookup"><span data-stu-id="a5574-105">Describes the DLNA device types that are supported by the Media Streaming API.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5574-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5574-106">Syntax</span></span>


```C++
typedef enum DeviceTypes { 
  Unknown               = 0x0,
  DigitalMediaRenderer  = 0x1,
  DigitalMediaServer    = 0x2,
  DigitalMediaPlayer    = 0x4
} DeviceTypes;
```



## <a name="constants"></a><span data-ttu-id="a5574-107">常數</span><span class="sxs-lookup"><span data-stu-id="a5574-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a5574-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知**</span><span class="sxs-lookup"><span data-stu-id="a5574-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="a5574-109">未知的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="a5574-109">Unknown device type.</span></span>

</dd> <dt>

<span data-ttu-id="a5574-110"><span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="a5574-110"><span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**</span></span>
</dt> <dd>

<span data-ttu-id="a5574-111">DLNA 數位媒體轉譯器 (DMR) 。</span><span class="sxs-lookup"><span data-stu-id="a5574-111">DLNA Digital Media Renderer (DMR).</span></span> <span data-ttu-id="a5574-112">值相當於裝置類型 **urn：架構-upnp-org： device： MediaRenderer： 1**。</span><span class="sxs-lookup"><span data-stu-id="a5574-112">The value is equivalent to the device type **urn:schemas-upnp-org:device:MediaRenderer:1**.</span></span>

</dd> <dt>

<span data-ttu-id="a5574-113"><span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**</span><span class="sxs-lookup"><span data-stu-id="a5574-113"><span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**</span></span>
</dt> <dd>

<span data-ttu-id="a5574-114"> (DMS) 的 DLNA 數位媒體伺服器。</span><span class="sxs-lookup"><span data-stu-id="a5574-114">DLNA Digital Media Server (DMS).</span></span> <span data-ttu-id="a5574-115">值相當於裝置類型 **urn：架構-upnp-org： device： MediaServer： 1**。</span><span class="sxs-lookup"><span data-stu-id="a5574-115">The value is equivalent to the device type **urn:schemas-upnp-org:device:MediaServer:1**.</span></span>

</dd> <dt>

<span data-ttu-id="a5574-116"><span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="a5574-116"><span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**</span></span>
</dt> <dd>

<span data-ttu-id="a5574-117">DLNA 數位媒體播放機</span><span class="sxs-lookup"><span data-stu-id="a5574-117">DLNA Digital Media Player</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5574-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5574-118">Requirements</span></span>



| <span data-ttu-id="a5574-119">需求</span><span class="sxs-lookup"><span data-stu-id="a5574-119">Requirement</span></span> | <span data-ttu-id="a5574-120">值</span><span class="sxs-lookup"><span data-stu-id="a5574-120">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5574-121">Idl</span><span class="sxs-lookup"><span data-stu-id="a5574-121">IDL</span></span><br/> | <dl> <span data-ttu-id="a5574-122"><dt> (參考) 的 windows...。 </dt></span><span class="sxs-lookup"><span data-stu-id="a5574-122"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





