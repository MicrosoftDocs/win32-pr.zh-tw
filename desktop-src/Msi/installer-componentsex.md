---
description: 傳回 RecordList 物件，這個物件會列出已安裝的元件。
ms.assetid: a91656de-2ebc-45b5-86f8-b13f35c6a762
title: ComponentsEx 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a48261a924280999d2b8329d635d4115de35753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990709"
---
# <a name="installercomponentsex-property"></a><span data-ttu-id="c02fd-103">ComponentsEx 屬性</span><span class="sxs-lookup"><span data-stu-id="c02fd-103">Installer.ComponentsEx property</span></span>

<span data-ttu-id="c02fd-104">這個屬性會傳回 [**RecordList**](recordlist-object.md) 物件，其中會列出已安裝的元件。</span><span class="sxs-lookup"><span data-stu-id="c02fd-104">This property returns a [**RecordList**](recordlist-object.md) object that lists installed components.</span></span> <span data-ttu-id="c02fd-105">這個屬性會呼叫 [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)。</span><span class="sxs-lookup"><span data-stu-id="c02fd-105">This property calls [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa).</span></span>

<span data-ttu-id="c02fd-106">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="c02fd-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="c02fd-107">從 Windows Installer 5.0 開始，可以使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c02fd-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="c02fd-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c02fd-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c02fd-109">語法</span><span class="sxs-lookup"><span data-stu-id="c02fd-109">Syntax</span></span>


```JScript
propVal = Installer.ComponentsEx
```



## <a name="property-value"></a><span data-ttu-id="c02fd-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="c02fd-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="c02fd-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="c02fd-111">Requirements</span></span>



| <span data-ttu-id="c02fd-112">需求</span><span class="sxs-lookup"><span data-stu-id="c02fd-112">Requirement</span></span> | <span data-ttu-id="c02fd-113">值</span><span class="sxs-lookup"><span data-stu-id="c02fd-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c02fd-114">版本</span><span class="sxs-lookup"><span data-stu-id="c02fd-114">Version</span></span><br/> | <span data-ttu-id="c02fd-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5。0</span><span class="sxs-lookup"><span data-stu-id="c02fd-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="c02fd-116">DLL</span><span class="sxs-lookup"><span data-stu-id="c02fd-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="c02fd-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c02fd-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="c02fd-118">IID</span><span class="sxs-lookup"><span data-stu-id="c02fd-118">IID</span></span><br/>     | <span data-ttu-id="c02fd-119">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c02fd-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="c02fd-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c02fd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c02fd-121">**MsiEnumComponentsEx**</span><span class="sxs-lookup"><span data-stu-id="c02fd-121">**MsiEnumComponentsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
</dt> </dl>

 

 




