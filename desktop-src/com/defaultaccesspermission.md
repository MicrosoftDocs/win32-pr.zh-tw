---
title: DefaultAccessPermission
description: 設定存取控制清單 (ACL) 可存取沒有 AccessPermission 設定之類別的主體。
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- DefaultAccessPermission 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c132096807b8c234259071758ebd361421f8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969836"
---
# <a name="defaultaccesspermission"></a>DefaultAccessPermission

設定存取控制清單 (ACL) 可存取沒有 [**AccessPermission**](accesspermission.md) 設定之類別的主體。 此 ACL 僅供未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的應用程式使用，而且在其 [**AppID**](appid-key.md)金鑰底下沒有 **AccessPermission** 值。

> [!Caution]  
> 不建議您變更這個值，因為這會影響所有未設定整個進程安全性的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。 如果您要變更此值，以影響特定 COM 應用程式的安全性設定，您應該改為變更該特定 COM 應用程式的整個進程安全性設定。 如需設定整個進程安全性的詳細資訊，請參閱 [設定整個進程的安全性](setting-processwide-security.md)。

 

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultAccessPermission = ACL
```

## <a name="remarks"></a>備註

這是 **REG \_ 二進位** 值。

伺服器中的 COM 執行時間會在模擬嘗試連接至物件的呼叫端時，檢查此值所描述的 ACL，而且其 success 會判斷是否允許或不允許存取。 如果存取檢查失敗，則不允許與物件的連接。 如果這個命名值不存在，則只允許伺服器主體和本機系統呼叫伺服器。

依預設，此值沒有任何專案。 只有伺服器主體和系統允許呼叫伺服器。

此值提供簡單的集中式系統管理，讓您能夠在電腦上執行物件的預設連接存取。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**AccessPermission**](accesspermission.md)
</dt> <dt>

[註冊 COM 伺服器](registering-com-servers.md)
</dt> <dt>

[設定整個進程的安全性](setting-processwide-security.md)
</dt> </dl>

 

 




