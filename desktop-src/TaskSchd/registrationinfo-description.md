---
title: RegistrationInfo。 Description 屬性
description: 針對腳本，取得或設定工作的描述。
ms.assetid: bb85fa09-155c-452b-bf6e-28ac4f60cc42
keywords:
- Description 屬性工作排程器
- Description 屬性工作排程器，RegistrationInfo 物件
- RegistrationInfo 物件工作排程器、Description 屬性
topic_type:
- apiref
api_name:
- RegistrationInfo.Description
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea6f141eddc40b21f1cf49e490fe30df5844e6029f821d9811b0e62ea55fa8ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872458"
---
# <a name="registrationinfodescription-property"></a>RegistrationInfo。 Description 屬性

針對腳本，取得或設定工作的描述。

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Description As String
```



## <a name="property-value"></a>屬性值

工作的描述。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**description**](taskschedulerschema-description-registrationinfotype-element.md) 元素來指定工作的描述。

設定這個屬性值時，值可以是從資源 .dll 檔抓取的文字。 特製化的字串會用來參考資源檔中的文字。 字串的格式為 $ ( @ \[ Dll \] 、 \[ ResourceID \]) 其中 \[ Dll \] 是包含資源的 .dll 檔案的路徑，而 \[ resourceid \] 是資源文字的識別碼。 例如，將此屬性值設定為 $ ( @% SystemRoot% \\ system32 \\ResourceName.dll，-101) 會將屬性設定為% SystemRoot% System32ResourceName.dll 檔中識別碼等於-101 的資源文字值 \\ \\ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





