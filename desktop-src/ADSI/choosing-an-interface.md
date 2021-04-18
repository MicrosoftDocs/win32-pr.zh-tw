---
title: 選擇系結的介面
description: 當目錄物件系結至時，呼叫端會指定所需的 ADSI 介面型別。
ms.assetid: 3c86e136-6d82-4baf-9c76-27dac8ad68ac
ms.tgt_platform: multiple
keywords:
- ADSI ADSI，使用，選擇要系結的介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444bd41d1567849d5bf3a85ac3ec22f317ced5d3
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382842"
---
# <a name="choosing-an-interface-for-binding"></a>選擇系結的介面

當目錄物件系結至時，呼叫端會指定所需的 ADSI 介面型別。 所有 ADSI 目錄物件都支援 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面。 ADSI 物件也可以支援其他介面。 物件所支援的實際介面取決於物件的類別。 例如，使用者物件可支援 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) 介面，但不支援 [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) 介面。

Automation 用戶端應該使用 **IADs \*** 介面，因為這些介面是雙重介面，可提供更高層級的抽象概念，並使用 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)資料類型提供資料。

除了 **\* IADs** 介面，C/c + + 用戶端還可以使用 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)和 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面。 這些介面不是雙重介面，且不支援 automation。 這些介面可讓您更精確地控制要取出哪些屬性，以及允許存取儲存在屬性中的原始資料。 例如，使用 [**IADs：： get**](/windows/desktop/api/Iads/nf-iads-iads-get)方法來取得物件的 **ntSecurityDescriptor** 屬性時， **IADs：： Get** 方法會提供支援 [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)介面的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面指標。 **IADsSecurityDescriptor** 介面是由 ADSI 提供以代表安全描述項。 相較之下，當使用 [**IDirectoryObject：： GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) 方法來抓取 **ntSecurityDescriptor** 屬性時， **IDirectoryObject：： GetObjectAttributes** 會提供可轉換成 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) 結構的位元組陣列。 Win32 安全性 Api 可以與此資料搭配使用，以操作安全描述項。

 

 