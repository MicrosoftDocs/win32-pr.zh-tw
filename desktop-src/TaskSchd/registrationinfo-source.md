---
title: RegistrationInfo。 Source 屬性
description: 針對腳本，取得或設定工作源自的位置。 例如，工作可能源自元件、服務、應用程式或使用者。
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Source 屬性工作排程器
- Source 屬性工作排程器，RegistrationInfo 物件
- RegistrationInfo 物件工作排程器、Source 屬性
topic_type:
- apiref
api_name:
- RegistrationInfo.Source
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97320d63823599e52327533afdba62f795622263e57878515ddd7ade9c98070b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126028"
---
# <a name="registrationinfosource-property"></a>RegistrationInfo。 Source 屬性

針對腳本，取得或設定工作源自的位置。 例如，工作可能源自元件、服務、應用程式或使用者。

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a>屬性值

工作源自的位置。 例如，從元件、服務、應用程式或使用者。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**source**](taskschedulerschema-source-registrationinfotype-element.md) 元素來指定工作來源資訊。

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

 

 





