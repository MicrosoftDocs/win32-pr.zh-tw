---
description: 提供 IMFMuxStreamAttributesManager 的實例，此實例會管理描述多工媒體來源子串流的 IMFAttributes。
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: 'MF_DEVICESTREAM_MULTIPLEXED_MANAGER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495b4054337aaa709bee430ae78ff4bed658911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975001"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a><span data-ttu-id="cafbc-103">MF \_ DEVICESTREAM 多工 \_ \_ 管理器屬性</span><span class="sxs-lookup"><span data-stu-id="cafbc-103">MF\_DEVICESTREAM\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="cafbc-104">提供 [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) 的實例，此實例會管理描述多工媒體來源子串流的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 。</span><span class="sxs-lookup"><span data-stu-id="cafbc-104">Provides an instance of [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) which manages the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) describing the substreams of a multiplexed media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="cafbc-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="cafbc-105">Data type</span></span>

<span data-ttu-id="cafbc-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="cafbc-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="cafbc-107">備註</span><span class="sxs-lookup"><span data-stu-id="cafbc-107">Remarks</span></span>

<span data-ttu-id="cafbc-108">將此值傳遞至 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) ，以判斷媒體來源是否提供多工資料流程，如果是，則取得 [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager)的實例。</span><span class="sxs-lookup"><span data-stu-id="cafbc-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to determine if the media source provides multiplexed streams and, if so, get an instance of [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="cafbc-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="cafbc-109">Requirements</span></span>



| <span data-ttu-id="cafbc-110">需求</span><span class="sxs-lookup"><span data-stu-id="cafbc-110">Requirement</span></span> | <span data-ttu-id="cafbc-111">值</span><span class="sxs-lookup"><span data-stu-id="cafbc-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cafbc-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cafbc-112">Minimum supported client</span></span><br/> | <span data-ttu-id="cafbc-113">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cafbc-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cafbc-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cafbc-114">Minimum supported server</span></span><br/> | <span data-ttu-id="cafbc-115">都不支援</span><span class="sxs-lookup"><span data-stu-id="cafbc-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="cafbc-116">標頭</span><span class="sxs-lookup"><span data-stu-id="cafbc-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="cafbc-117"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cafbc-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
