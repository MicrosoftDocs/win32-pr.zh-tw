---
description: 提供 IMFMuxStreamMediaTypeManager 的實例，可用來取得多工媒體來源子串流的媒體類型，以及控制由來源進行多工的子串流的組合。
ms.assetid: 5C36956D-336A-4956-8793-D86DC792E906
title: 'MF_MEDIATYPE_MULTIPLEXED_MANAGER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa96c74bbff8f4858c8467fcd13253cfedf2f5dc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104195728"
---
# <a name="mf_mediatype_multiplexed_manager-attribute"></a><span data-ttu-id="b9e13-103">MF \_ 媒體多工 \_ \_ 管理器屬性</span><span class="sxs-lookup"><span data-stu-id="b9e13-103">MF\_MEDIATYPE\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="b9e13-104">提供 [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) 的實例，可用來取得多工媒體來源子串流的媒體類型，以及控制由來源進行多工的子串流的組合。</span><span class="sxs-lookup"><span data-stu-id="b9e13-104">Provides an instance of [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) which can be used to get the media types of the substreams of a multiplexed media source as well as control the combination of substreams that are multiplexed by the source.</span></span>

## <a name="data-type"></a><span data-ttu-id="b9e13-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b9e13-105">Data type</span></span>

<span data-ttu-id="b9e13-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="b9e13-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="b9e13-107">備註</span><span class="sxs-lookup"><span data-stu-id="b9e13-107">Remarks</span></span>

<span data-ttu-id="b9e13-108">將此值傳遞至 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) ，以取得 [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager)的實例。</span><span class="sxs-lookup"><span data-stu-id="b9e13-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to get an instance of [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9e13-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9e13-109">Requirements</span></span>



| <span data-ttu-id="b9e13-110">需求</span><span class="sxs-lookup"><span data-stu-id="b9e13-110">Requirement</span></span> | <span data-ttu-id="b9e13-111">值</span><span class="sxs-lookup"><span data-stu-id="b9e13-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e13-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9e13-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b9e13-113">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9e13-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b9e13-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9e13-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b9e13-115">都不支援</span><span class="sxs-lookup"><span data-stu-id="b9e13-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="b9e13-116">標頭</span><span class="sxs-lookup"><span data-stu-id="b9e13-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9e13-117"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b9e13-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
