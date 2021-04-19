---
description: 傳回 RecordList 物件，這個物件會提供指定已安裝元件的完整路徑。
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: ComponentPathEx 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPathEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b7bf98dd8e7a81a0dd261f22a565bec8298a86a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977558"
---
# <a name="installercomponentpathex-property"></a><span data-ttu-id="9189c-103">ComponentPathEx 屬性</span><span class="sxs-lookup"><span data-stu-id="9189c-103">Installer.ComponentPathEx property</span></span>

<span data-ttu-id="9189c-104">這個屬性會傳回 [**RecordList**](recordlist-object.md) 物件，該物件會提供指定已安裝元件的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="9189c-104">This property returns a [**RecordList**](recordlist-object.md) object that gives the full path of a specified installed component.</span></span> <span data-ttu-id="9189c-105">這個屬性會呼叫 [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)。</span><span class="sxs-lookup"><span data-stu-id="9189c-105">This property calls [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).</span></span>

<span data-ttu-id="9189c-106">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="9189c-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="9189c-107">從 Windows Installer 5.0 開始，可以使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="9189c-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="9189c-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9189c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9189c-109">語法</span><span class="sxs-lookup"><span data-stu-id="9189c-109">Syntax</span></span>


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a><span data-ttu-id="9189c-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="9189c-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="9189c-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="9189c-111">Requirements</span></span>



| <span data-ttu-id="9189c-112">需求</span><span class="sxs-lookup"><span data-stu-id="9189c-112">Requirement</span></span> | <span data-ttu-id="9189c-113">值</span><span class="sxs-lookup"><span data-stu-id="9189c-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9189c-114">版本</span><span class="sxs-lookup"><span data-stu-id="9189c-114">Version</span></span><br/> | <span data-ttu-id="9189c-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5。0</span><span class="sxs-lookup"><span data-stu-id="9189c-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="9189c-116">DLL</span><span class="sxs-lookup"><span data-stu-id="9189c-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="9189c-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9189c-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="9189c-118">IID</span><span class="sxs-lookup"><span data-stu-id="9189c-118">IID</span></span><br/>     | <span data-ttu-id="9189c-119">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9189c-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="9189c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9189c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9189c-121">**MsiGetComponentPathEx**</span><span class="sxs-lookup"><span data-stu-id="9189c-121">**MsiGetComponentPathEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




