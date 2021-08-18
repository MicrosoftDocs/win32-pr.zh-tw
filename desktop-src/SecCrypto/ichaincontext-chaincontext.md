---
description: 設定或抓取憑證的 PCCERT \_ 鏈 \_ 內容。
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: IChainCoNtext：： ChainCoNtext 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d5e7bc92aa798766538af19cae440542705a859040aed7fc8d9510e3724051f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005496"
---
# <a name="ichaincontextchaincontext-property"></a>IChainCoNtext：： ChainCoNtext 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。\]

**ChainCoNtext** 屬性會設定或抓取憑證的 PCCERT \_ 鏈 \_ 內容。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a>屬性值

憑證的 PCCERT \_ 鏈 \_ 內容。

## <a name="error-codes"></a>錯誤碼

如果屬性存取方法 **put \_ ChainCoNtext** 並 **讓 \_ ChainCoNtext** 成功，則會傳回 S \_ OK。

任何其他 **HRESULT** 值都表示呼叫失敗。

## <a name="remarks"></a>備註

您必須呼叫 [**FreeCoNtext**](ichaincontext-freecontext.md) 方法或 [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) 函數來釋放內容。

如果您設定 **ChainCoNtext** 屬性，則會重設整個 [**鏈**](chain.md) 物件的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IChainCoNtext**](ichaincontext.md)
</dt> </dl>

 

 




