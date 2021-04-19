---
description: 包含連接的圖示檔路徑。
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: ICONFilePath (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: 6b1e98f76fe2f83ce214076223b5a1439bd0ea45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998458"
---
# <a name="iconfilepath-mbnprofile-element"></a><span data-ttu-id="e5093-103">ICONFilePath (MBNProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="e5093-103">ICONFilePath (MBNProfile) Element</span></span>

<span data-ttu-id="e5093-104">**ICONFilePath (MBNProfile)** 元素包含連接的圖示檔路徑。</span><span class="sxs-lookup"><span data-stu-id="e5093-104">The **ICONFilePath (MBNProfile)** element contains the path of the icon file for the connection.</span></span>

<span data-ttu-id="e5093-105">當使用此專案進行連接時，作業系統連接 UI 會顯示此圖示。</span><span class="sxs-lookup"><span data-stu-id="e5093-105">The operating system connection UI will display this icon when a connection is made using this element.</span></span>

<span data-ttu-id="e5093-106">在 [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager)介面的 [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile)方法中傳遞用來建立設定檔的 XML 時，此路徑應指向圖示檔的來源位置。</span><span class="sxs-lookup"><span data-stu-id="e5093-106">When passing the XML for creating the profile in the [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) method of the [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) interface, this path should point to the source location of the icon file.</span></span> <span data-ttu-id="e5093-107">在成功建立 [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) 物件時，行動寬頻服務會複製其內部存放區中的圖示檔，並且會修改設定檔路徑以反映此情況。</span><span class="sxs-lookup"><span data-stu-id="e5093-107">On successful creation of [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) object, the Mobile Broadband service will copy the icon file in it's internal store and the profile path will be modified to reflect this.</span></span>

<span data-ttu-id="e5093-108">圖示檔的格式應為具有32X32 圖元維度的 .bmp 格式。</span><span class="sxs-lookup"><span data-stu-id="e5093-108">The icon file should be in .bmp format with 32X32 pixel dimension.</span></span>

<span data-ttu-id="e5093-109">此元素是長度最多為1024個字元的字串，其中包含絕對檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="e5093-109">This element is a string of length up to 1024 characters, containing an absolute file path.</span></span>

<span data-ttu-id="e5093-110">元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="e5093-110">The element is optional.</span></span>

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

<span data-ttu-id="e5093-111">**ICONFilePath** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="e5093-111">The **ICONFilePath** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5093-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5093-112">Requirements</span></span>



| <span data-ttu-id="e5093-113">需求</span><span class="sxs-lookup"><span data-stu-id="e5093-113">Requirement</span></span> | <span data-ttu-id="e5093-114">值</span><span class="sxs-lookup"><span data-stu-id="e5093-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="e5093-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5093-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e5093-116">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5093-116">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="e5093-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5093-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e5093-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="e5093-118">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="e5093-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5093-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="e5093-120">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="e5093-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e5093-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="e5093-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="e5093-122">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="e5093-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e5093-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="e5093-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




