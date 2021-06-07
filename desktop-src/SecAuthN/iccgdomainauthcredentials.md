---
description: 用戶端執行的介面，可讓開發人員在執行時間動態提供自己的認證，以使用 Active Directory 來驗證未加入網域的容器。
title: 'ICcgDomainAuthCredentials 介面 (ccgplugins .h) '
ms.topic: reference
ms.date: 10/20/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials
api_type:
- COM
api_location:
- ccgplugins.dll
ms.openlocfilehash: 8217f806ff0a1a6b38d045c7f665758ccaf8b1f5
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387806"
---
# <a name="iccgdomainauthcredentials-interface"></a>ICcgDomainAuthCredentials 介面

用戶端執行的介面，可讓開發人員在執行時間動態提供自己的認證，以使用 Active Directory 來驗證未加入網域的容器。 

## <a name="members"></a>成員

**ICcgDomainAuthCredentials** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ICcgDomainAuthCredentials** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ICcgDomainAuthCredentials** 介面具有這些方法。



| 方法                                           | 描述                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**GetPasswordCredentials**](iccgdomainauthcredentials-getpasswordcredentials.md)               | 傳回認證，以使用 Active Directory 驗證未加入網域的容器。<br/>                                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>ccgplugins。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>ccgplugins .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>ccgplugins.dll</dt> </dl> |
| IID<br/>                      | 6ecda518-2010-4437-8bc3-46e752b7b172<br/>          |



 

