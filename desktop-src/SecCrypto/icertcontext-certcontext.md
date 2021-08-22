---
description: 設定或抓取憑證的 PCCERT \_ 內容。
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: ICertCoNtext：： CertCoNtext 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5c517384bdffd8723c1e9e0d96683cc4bd4918361acdf19df77286bfbac962b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006366"
---
# <a name="icertcontextcertcontext-property"></a>ICertCoNtext：： CertCoNtext 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。\]

**CertCoNtext** 屬性會設定或抓取憑證的 PCCERT \_ 內容。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a>屬性值

憑證的 PCCERT \_ 內容。

## <a name="error-codes"></a>錯誤碼

如果屬性存取方法 **put \_ CertCoNtext** 並 **讓 \_ CertCoNtext** 成功，則會傳回 S \_ OK。

任何其他 **HRESULT** 值都表示呼叫失敗。

## <a name="remarks"></a>備註

您必須呼叫 [**FreeCoNtext**](icertcontext-freecontext.md) 方法或 [**CertFreeCertificateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) 函數來釋放內容。

如果您設定 **CertCoNtext** 屬性，則會重設整個 [**憑證**](certificate.md) 物件的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICertCoNtext**](icertcontext.md)
</dt> </dl>

 

 




