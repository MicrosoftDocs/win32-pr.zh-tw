---
description: 傳回字串，其中包含有關已編制索引之專案的其他錯誤資訊。
ms.assetid: 4f0d5289-c414-4e2b-b612-be8ce1d98b12
title: IChain2：： ExtendedErrorInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ExtendedErrorInfo
- IChain2.ExtendedErrorInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f8a7840d0f54ea7e93ad9998d5e8772a2ae411f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994139"
---
# <a name="ichain2extendederrorinfo-method"></a>IChain2：： ExtendedErrorInfo 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Chain 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1)。\]

**ExtendedErrorInfo** 方法會傳回字串，其中包含有關已編制索引之專案的其他錯誤資訊。

此方法是在 CAPICOM 2.0 中引進。

## <a name="syntax"></a>語法


```VB
Chain.ExtendedErrorInfo( _
  [ ByVal Index ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在中，選擇性\]
</dt> <dd>

**Long** ，代表專案的索引。 預設值為1，這會在鏈中傳回終端憑證的錯誤資訊。 Certificate **。 Count** 會傳回有關鏈根憑證的資訊。 0會傳回整個鏈的延伸錯誤資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

字串，包含擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**鏈**](chain.md)
</dt> </dl>

 

 
