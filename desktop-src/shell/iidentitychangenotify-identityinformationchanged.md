---
description: IdentityInformationChanged 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 3aca8a98-3d12-482d-9991-d6b53adde522
title: 'IIdentityChangeNotify：： IdentityInformationChanged 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.IdentityInformationChanged
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 58e146812bb36a9ff8e692aa424f328abc6eb62e47b98abb1deef2b4e919af40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821918"
---
# <a name="iidentitychangenotifyidentityinformationchanged-method"></a>IIdentityChangeNotify：： IdentityInformationChanged 方法

\[**IdentityInformationChanged** 不受支援，未來可能會變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

當使用者身分識別的相關資訊變更，或新增或刪除使用者身分識別時呼叫。

## <a name="syntax"></a>語法


```C++
HRESULT IdentityInformationChanged(
   DWORD dwType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwType* 
</dt> <dd>

類型： **DWORD**

值，指定變更的資訊類型，或針對身分識別所執行的作業。 可以是下列值的組合。

<dt>



  (IIC \_ 目前的身分 \_ 識別 \_ 已變更) 


</dt> <dd>

目前的身分識別已修改。

</dd> <dt>



  (IIC 身分 \_ 識別 \_ 已變更) 


</dt> <dd>

已修改身分識別。

</dd> <dt>



  (已刪除的 IIC 身分 \_ 識別 \_) 


</dt> <dd>

已刪除身分識別。

</dd> <dt>



  (新增的 IIC 身分 \_ 識別 \_) 


</dt> <dd>

已新增身分識別。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

當系統上的使用者身分識別清單已修改時，您可以執行此方法，以提供應用程式的自訂行為。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows 2000 Professional<br/>                                                   |
| 伺服器支援結束<br/>    | Windows 2000 Server<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



 

 




