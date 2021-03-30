---
description: IEnumUserIdentity 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: df4b6235-e66a-4187-b1f9-33c042cae2f2
title: 'IEnumUserIdentity 介面 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 48abf182942f90ecd477a241be3bf45323bdbdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973124"
---
# <a name="ienumuseridentity-interface"></a>IEnumUserIdentity 介面

\[**IEnumUserIdentity** 不受支援，未來可能會變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

提供系統上所有使用者身分識別的列舉。

## <a name="members"></a>成員

**IEnumUserIdentity** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IEnumUserIdentity** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IEnumUserIdentity** 介面具有這些方法。



| 方法                                         | 描述                                                                                                                  |
|:-----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**克隆**](ienumuseridentity-clone.md)       | 已取代。 取得目前列舉的複本。<br/>                                                               |
| [**GetCount**](ienumuseridentity-getcount.md) | 已取代。 取得目前在系統上的使用者身分識別計數。<br/>                                            |
| [**下一步**](ienumuseridentity-next.md)         | 已取代。 從列舉中抓取使用者識別介面的陣列。<br/>                                  |
| [**重設**](ienumuseridentity-reset.md)       | 已取代。 重設列舉中已抓取介面的內部計數。<br/>                                 |
| [**跳過**](ienumuseridentity-skip.md)         | 已取代。 在列舉中略過指定數目的使用者識別介面。 在抓取介面時使用。<br/> |



 

## <a name="remarks"></a>備註

若要取得系統上存在的使用者身分識別相關資訊，您可以使用此介面。 從 [**IUserIdentityManager**](iuseridentitymanager.md) 介面中，您可以呼叫 [**IUserIdentityManager：： EnumIdentities**](iuseridentitymanager-enumidentities.md) 以抓取這個介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                  |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> </dl>

 

 
