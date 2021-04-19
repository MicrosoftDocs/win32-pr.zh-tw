---
description: 指定音訊串流的裝置角色。
ms.assetid: E4B7660D-5F41-495A-B77D-94B7981F4C2C
title: MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b1b00115a28592140e41463cf296acf54ad7cde
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982140"
---
# <a name="mf_media_engine_audio_endpoint_role-attribute"></a><span data-ttu-id="d9b2b-103">MF \_ 媒體 \_ 引擎 \_ 音訊 \_ 端點 \_ 角色屬性</span><span class="sxs-lookup"><span data-stu-id="d9b2b-103">MF\_MEDIA\_ENGINE\_AUDIO\_ENDPOINT\_ROLE attribute</span></span>

<span data-ttu-id="d9b2b-104">指定音訊串流的裝置角色。</span><span class="sxs-lookup"><span data-stu-id="d9b2b-104">Specifies the device role for the audio stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="d9b2b-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="d9b2b-105">Data type</span></span>

<span data-ttu-id="d9b2b-106">**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="d9b2b-106">**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d9b2b-107">備註</span><span class="sxs-lookup"><span data-stu-id="d9b2b-107">Remarks</span></span>

<span data-ttu-id="d9b2b-108">這個屬性的值是 [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="d9b2b-108">The value of this attribute is a member of the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration.</span></span>

<span data-ttu-id="d9b2b-109">這個屬性會與 [**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) 方法搭配使用，以初始化 Media Engine。</span><span class="sxs-lookup"><span data-stu-id="d9b2b-109">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span> <span data-ttu-id="d9b2b-110">屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="d9b2b-110">The attribute is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9b2b-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9b2b-111">Requirements</span></span>



| <span data-ttu-id="d9b2b-112">需求</span><span class="sxs-lookup"><span data-stu-id="d9b2b-112">Requirement</span></span> | <span data-ttu-id="d9b2b-113">值</span><span class="sxs-lookup"><span data-stu-id="d9b2b-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b2b-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d9b2b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d9b2b-115">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9b2b-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="d9b2b-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d9b2b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d9b2b-117">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9b2b-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d9b2b-118">標頭</span><span class="sxs-lookup"><span data-stu-id="d9b2b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9b2b-119"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d9b2b-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9b2b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9b2b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b2b-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="d9b2b-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
