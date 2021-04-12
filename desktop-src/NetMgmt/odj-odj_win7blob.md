---
title: ODJ_WIN7BLOB
description: ODJ_WIN7BLOB IDL 定義
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 2083648636bd58c64314ba22852839f89ed4461d
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104316705"
---
# <a name="odj_win7blob-structure"></a>ODJ_WIN7BLOB 結構

包含將用戶端加入網域所需的基本資訊。

## <a name="syntax"></a>語法

```C++
typedef struct _ODJ_WIN7BLOB
{
    [string] wchar_t *lpDomain;
    [string] wchar_t *lpMachineName;
    [string] wchar_t *lpMachinePassword;
    ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
    DOMAIN_CONTROLLER_INFOW DcInfo;
    DWORD Options;
} ODJ_WIN7BLOB;
```

## <a name="members"></a>成員

### <a name="lpdomain"></a>lpDomain

必須設定為功能變數名稱。

### <a name="lpmachinename"></a>lpMachineName

必須設定為電腦名稱稱。

### <a name="lpmachinepassword"></a>lpMachinePassword

必須針對 lpMachineName 所識別的電腦帳戶設定為純文字密碼

### <a name="dnsdomaininfo"></a>DnsDomainInfo

包含要聯結之網域的相關資訊。

### <a name="dcinfo"></a>DcInfo

包含用來建立電腦帳戶 Active Directory 之網域控制站的命名和定址資訊。

### <a name="options"></a>選項

必須設定為零。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)

[**ODJ \_ 原則 \_ DNS \_ 網域 \_ 資訊**](odj-odj_policy_dns_domain_info.md)

[**DOMAIN_CONTROLLER_INFOW**](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



