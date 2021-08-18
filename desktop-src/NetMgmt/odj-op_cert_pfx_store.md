---
title: OP_CERT_PFX_STORE
description: OP_CERT_PFX_STORE IDL 定義
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 28e8b9e1a6d73f3d93e1700f812b21a0edf21982b7d5b9c927f4e7391b961850
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911538"
---
# <a name="op_cert_pfx_store-structure"></a>OP_CERT_PFX_STORE 結構

包含序列化的 PFX 結構。

## <a name="syntax"></a>語法

```C++
typedef struct _OP_CERT_PFX_STORE
{
    [string] wchar_t            *pTemplateName;
    ULONG                       ulPrivateKeyExportPolicy;
    [string] wchar_t            *pPolicyServerUrl;
    ULONG                       ulPolicyServerUrlFlags;
    [string] wchar_t            *pPolicyServerId;
    ULONG                       cbPfx;
    [size_is(cbPfx)]    PBYTE   pPfx;
} OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;
```

## <a name="members"></a>成員

### <a name="ptemplatename"></a>pTemplateName

必須設定為用來建立憑證的憑證範本名稱。

### <a name="ulprivatekeyexportpolicy"></a>ulPrivateKeyExportPolicy

包含 [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) 列舉中的一個值。

### <a name="ppolicyserverurl"></a>pPolicyServerUrl

必須設定原則伺服器的 URL。

### <a name="ulpolicyserverurlflags"></a>ulPolicyServerUrlFlags

包含 [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) 列舉中的一個值。

### <a name="ppolicyserverid"></a>pPolicyServerId

包含可唯一識別原則伺服器的字串

### <a name="cbpfx"></a>cbPfx

包含 pPfx 的大小（以位元組為單位）。

### <a name="ppfx"></a>pPfx

包含序列化的 PFX 結構 (請參閱 [**RFC 7292**](https://tools.ietf.org/html/rfc7292)) 。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)
