---
description: 指定代表感應器轉換所需裝置功能的 unicode 字串清單。
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: 'MF_DEVICESTREAM_REQUIRED_CAPABILITIES 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cac47d60c38e41d44ecf0776ea8bf7588559dfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113673"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a><span data-ttu-id="b3105-103">MF \_ DEVICESTREAM \_ 需要的 \_ 功能屬性</span><span class="sxs-lookup"><span data-stu-id="b3105-103">MF\_DEVICESTREAM\_REQUIRED\_CAPABILITIES attribute</span></span>

<span data-ttu-id="b3105-104">指定代表感應器轉換所需裝置功能的 unicode 字串清單。</span><span class="sxs-lookup"><span data-stu-id="b3105-104">Specifies a list of unicode strings representing the device capabilities required by the sensor transform.</span></span>

## <a name="data-type"></a><span data-ttu-id="b3105-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b3105-105">Data type</span></span>

<span data-ttu-id="b3105-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="b3105-106">\**WCHAR\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="b3105-107">備註</span><span class="sxs-lookup"><span data-stu-id="b3105-107">Remarks</span></span>

<span data-ttu-id="b3105-108">這個屬性是選擇性的，只有在感應器轉換存取受保護的資源時才需要。</span><span class="sxs-lookup"><span data-stu-id="b3105-108">This attribute is optional and only required if the sensor transform accesses a protected resource.</span></span> <span data-ttu-id="b3105-109">此值必須是 [_ *DeviceCapability* \*](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability)中定義的字串標記清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="b3105-109">The value must be a semicolon delimited list of string tokens defined in [_ *DeviceCapability*\*](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3105-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3105-110">Requirements</span></span>



| <span data-ttu-id="b3105-111">需求</span><span class="sxs-lookup"><span data-stu-id="b3105-111">Requirement</span></span> | <span data-ttu-id="b3105-112">值</span><span class="sxs-lookup"><span data-stu-id="b3105-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3105-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3105-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b3105-114">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3105-114">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b3105-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3105-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b3105-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="b3105-116">None supported</span></span><br/>                                                          |
| <span data-ttu-id="b3105-117">標頭</span><span class="sxs-lookup"><span data-stu-id="b3105-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3105-118"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b3105-118"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
