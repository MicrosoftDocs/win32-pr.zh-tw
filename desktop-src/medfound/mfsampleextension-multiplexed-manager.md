---
description: 提供用來從多工媒體來源的子串流存取樣本集合的 IMFMuxStreamSampleManager 實例。
ms.assetid: 4FD8169D-FDDF-4C69-AD46-05B02B35028C
title: 'MFSampleExtension_MULTIPLEXED_MANAGER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b46c277265538ccb2b990ea9d912b9337bcd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979075"
---
# <a name="mfsampleextension_multiplexed_manager-attribute"></a><span data-ttu-id="dcfb4-103">MFSampleExtension 多工 \_ \_ 管理器屬性</span><span class="sxs-lookup"><span data-stu-id="dcfb4-103">MFSampleExtension\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="dcfb4-104">提供用來從多工媒體來源的子串流存取樣本集合的 [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager) 實例。</span><span class="sxs-lookup"><span data-stu-id="dcfb4-104">Provides an instance of [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager) which is used to access the collection of samples from the substreams of a multiplexed media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="dcfb4-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="dcfb4-105">Data type</span></span>

<span data-ttu-id="dcfb4-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="dcfb4-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="dcfb4-107">備註</span><span class="sxs-lookup"><span data-stu-id="dcfb4-107">Remarks</span></span>

<span data-ttu-id="dcfb4-108">將此值傳遞至 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) ，以取得 [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager)的實例。</span><span class="sxs-lookup"><span data-stu-id="dcfb4-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to get an instance of [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="dcfb4-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcfb4-109">Requirements</span></span>



| <span data-ttu-id="dcfb4-110">需求</span><span class="sxs-lookup"><span data-stu-id="dcfb4-110">Requirement</span></span> | <span data-ttu-id="dcfb4-111">值</span><span class="sxs-lookup"><span data-stu-id="dcfb4-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dcfb4-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dcfb4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="dcfb4-113">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dcfb4-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dcfb4-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dcfb4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="dcfb4-115">都不支援</span><span class="sxs-lookup"><span data-stu-id="dcfb4-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="dcfb4-116">標頭</span><span class="sxs-lookup"><span data-stu-id="dcfb4-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcfb4-117"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="dcfb4-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
