---
title: MDM_ClientCertificateInstall_Install03 類別的 EnrollMethod 方法
description: 觸發裝置以啟動憑證註冊。
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- EnrollMethod 方法
- EnrollMethod 方法，MDM_ClientCertificateInstall_Install03 類別
- MDM_ClientCertificateInstall_Install03 類別，EnrollMethod 方法
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03.EnrollMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ddeca621f58015aa3806212c1250aeb43554a51cbb28e15414e779571b9c102
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109398"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a>MDM \_ ClientCertificateInstall Install03 類別的 EnrollMethod \_ 方法

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

觸發裝置以啟動憑證註冊。 憑證註冊完成後，裝置將不會通知 MDM 伺服器。 MDM 伺服器稍後可以查詢裝置，以找出是否已新增新憑證。 另請參閱 [**註冊**](/windows/client-management/mdm/clientcertificateinstall-csp)。

## <a name="syntax"></a>語法


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

必要。 觸發裝置以啟動憑證註冊。 憑證註冊完成後，裝置將不會通知 MDM 伺服器。 MDM 伺服器稍後可以查詢裝置，以找出是否已新增新憑證。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MDM \_ ClientCertificateInstall \_ Install03**](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

