---
description: 將 managed 物件系結至應用程式域，也就是應用程式執行所在的隔離環境。
ms.assetid: 9357ea5d-6f86-4747-a923-16575ff13122
title: 'AppDomainHelper 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AppDomainHelper
api_type:
- COM
ms.openlocfilehash: bab1ade7d97d3e911dbe0dc56cff69c5308d7d5e44baadb4641829c5f5a9d806
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117917552"
---
# <a name="appdomainhelper-class"></a>AppDomainHelper 類別

將 managed 物件系結至應用程式域，也就是應用程式執行所在的隔離環境。

## <a name="when-to-implement"></a>執行時機

這個類別是由 COM + 所執行。



| 需求 | 值 |
|------------|-------------------------------------------------------|
| CLSID      | GUID \_ AppDomainHelper                                 |
| ProgID     | L "System.enterpriseservices. AppDomainHelper" |
| 介面 | [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)          |



 

## <a name="when-to-use"></a>使用時機

您可以使用這個類別來存取 [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)的方法。

## <a name="remarks"></a>備註

若要建立這個物件，請呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。

若要從 Microsoft Visual Basic 使用這個類別，請新增 com + 服務類型程式庫的參考。 您可以使用 "COMSVCSLib. AppDomainHelper" 將 AppDomainHelper 物件宣告為類別名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP （含 SP1） \[ 桌面應用程式\]<br/>                                 |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>ComSvcs。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)
</dt> </dl>

 

