---
description: 傳回 RecordList 物件，這個物件會列出使用指定已安裝元件的產品。
ms.assetid: c9756526-68d7-4d04-97e2-56a5eaf816be
title: ClientsEx 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClientsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5a609ab0ba6edc5b0e3e9bbd26bc3539858ebdee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989863"
---
# <a name="installerclientsex-property"></a><span data-ttu-id="d55fc-103">ClientsEx 屬性</span><span class="sxs-lookup"><span data-stu-id="d55fc-103">Installer.ClientsEx property</span></span>

<span data-ttu-id="d55fc-104">這個屬性會傳回 [**RecordList**](recordlist-object.md) 物件，其中會列出使用指定之已安裝元件的產品。</span><span class="sxs-lookup"><span data-stu-id="d55fc-104">This property returns a [**RecordList**](recordlist-object.md) object that lists products that use a specified installed component.</span></span> <span data-ttu-id="d55fc-105">這個屬性會呼叫 [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)。</span><span class="sxs-lookup"><span data-stu-id="d55fc-105">This property calls [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).</span></span>

<span data-ttu-id="d55fc-106">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="d55fc-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="d55fc-107">從 Windows Installer 5.0 開始，可以使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d55fc-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="d55fc-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d55fc-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d55fc-109">語法</span><span class="sxs-lookup"><span data-stu-id="d55fc-109">Syntax</span></span>


```JScript
propVal = Installer.ClientsEx
```



## <a name="property-value"></a><span data-ttu-id="d55fc-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="d55fc-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="d55fc-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d55fc-111">Requirements</span></span>



| <span data-ttu-id="d55fc-112">需求</span><span class="sxs-lookup"><span data-stu-id="d55fc-112">Requirement</span></span> | <span data-ttu-id="d55fc-113">值</span><span class="sxs-lookup"><span data-stu-id="d55fc-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d55fc-114">版本</span><span class="sxs-lookup"><span data-stu-id="d55fc-114">Version</span></span><br/> | <span data-ttu-id="d55fc-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5。0</span><span class="sxs-lookup"><span data-stu-id="d55fc-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="d55fc-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d55fc-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="d55fc-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d55fc-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="d55fc-118">IID</span><span class="sxs-lookup"><span data-stu-id="d55fc-118">IID</span></span><br/>     | <span data-ttu-id="d55fc-119">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d55fc-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="d55fc-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d55fc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d55fc-121">**MsiEnumClientsEx**</span><span class="sxs-lookup"><span data-stu-id="d55fc-121">**MsiEnumClientsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 




