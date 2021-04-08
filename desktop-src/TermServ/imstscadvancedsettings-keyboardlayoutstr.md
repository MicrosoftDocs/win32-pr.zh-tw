---
title: IMsTscAdvancedSettings KeyBoardLayoutStr 屬性
description: 指定使用中輸入地區設定識別碼的名稱 (先前稱為用於連接的鍵盤配置) 。
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- KeyBoardLayoutStr 屬性遠端桌面服務
- KeyBoardLayoutStr 屬性遠端桌面服務，IMsTscAdvancedSettings 介面
- IMsTscAdvancedSettings 介面遠端桌面服務，KeyBoardLayoutStr 屬性
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.KeyBoardLayoutStr
- IMsTscAdvancedSettings.put_KeyBoardLayoutStr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4d5e6703b86f5e60a50ead05f8015df61cfdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685908"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a>IMsTscAdvancedSettings：： KeyBoardLayoutStr 屬性

指定使用中輸入地區設定識別碼的名稱 (先前稱為用於連接的鍵盤配置) 。

如果未設定這個屬性，控制項會使用 [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) 函式所傳回的預設版面配置。

此屬性是唯寫的。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_KeyBoardLayoutStr(
  [in] BSTR KeyBoardLayoutStr
);
```



## <a name="property-value"></a>屬性值

現用輸入地區設定識別碼的名稱。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

屬性是字串形式的八位數十六進位數位。 下方四個數字代表語言識別項，而前四個數字代表該語言內的鍵盤變化。 例如，"00000409" 代表預設的美式英文鍵盤，因為 "0409" 是美國英文的語言識別項。 美式英文鍵盤的 Dvorak 變化具有 "00010409" 的識別碼。 您可以在下列的登錄中找到可用的鍵盤配置（依鍵盤配置識別碼列出）：

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                            |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings 定義為809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

