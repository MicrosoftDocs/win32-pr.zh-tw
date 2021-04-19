---
description: 顯示用來選取憑證的對話方塊，並傳回選取的憑證集合。
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: ICertificates2：： Select 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Select
- ICertificates2.Select
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cfd5b1cb5e269c14e05de25262fda711549bf02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997800"
---
# <a name="icertificates2select-method"></a>ICertificates2：： Select 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/previous-versions/windows/embedded/hh424013(v=msdn.10))。\]

**Select** 方法會顯示一個對話方塊來選取憑證，並傳回選取的憑證集合。 此方法是在 CAPICOM 2.0 中引進。

## <a name="syntax"></a>語法


```VB
Certificates.Select( _
  [ ByVal Title ], _
  [ ByVal DisplayString ], _
  [ ByVal bMultiSelect ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*標題* \[在中，選擇性\]
</dt> <dd>

字串，包含對話方塊的標題。 預設值為空字串 ("")。

</dd> <dt>

*DisplayString* \[在中，選擇性\]
</dt> <dd>

字串，包含對話方塊顯示的提示文字。 預設值為空字串 ("")。

</dd> <dt>

*bMultiSelect* \[在中，選擇性\]
</dt> <dd>

指出使用者是否可以選取多個憑證的布林值。 True 表示可以使用 CTRL 或 SHIFT 鍵選取多個憑證。 預設值為 false。

</dd> </dl>

## <a name="return-value"></a>傳回值

包含從對話方塊中選取之憑證的 [**憑證**](certificates.md) 物件。

**CAPICOM 2.1：** 傳回的 [**憑證**](certificates.md) 物件包含進行選取之集合中的憑證參考。 對傳回的 **憑證** 物件中的憑證所做的任何變更，都會反映在該集合中。

**Capicom 2.0、capicom 2.0.0.1、capicom 2.0.0.2 和 capicom 2.0.0.3：** 傳回的 [**憑證**](certificates.md) 物件包含從中進行選取之集合中的憑證複本。 對傳回的 **憑證** 物件中的憑證所做的任何變更都不會反映在該集合中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
