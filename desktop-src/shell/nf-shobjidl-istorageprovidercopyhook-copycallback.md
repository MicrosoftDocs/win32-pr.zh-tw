---
description: 決定是否允許 Shell 移動、複製、刪除或重新命名雲端提供者的同步根中的資料夾。
title: IStorageProviderCopyHook::CopyCallback
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook::CopyCallback
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: c7df9296f2261e3907702067ca36265095102f34
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104991842"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a>IStorageProviderCopyHook：： CopyCallback 方法

決定是否允許 Shell 移動、複製、刪除或重新命名雲端提供者的同步根中的資料夾。

## <a name="syntax"></a>語法

```C++
HRESULT CopyCallback( 
    HWND hwnd,
    UINT operation,
    UINT flags,
    LPCWSTR srcFile,
    DWORD srcAttribs,
    LPCWSTR destFile,
    DWORD destAttribs,
    UINT* result
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* \[在\]
</dt> <dd>

針對處理常式可能需要顯示之任何使用者介面元素的父代，複製攔截處理常式應該使用的視窗控制碼。 如果在 *作業中指定* **FOF_SILENT** ，則方法應忽略此參數。

</dd> </dl>

<dl> <dt>

*操作* \[在\]
</dt> <dd>

要執行的作業。 這個參數可以是 [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa)結構的 **wFunc** 成員下所列的其中一個值。

</dd> </dl>

<dl> <dt>

*旗標* \[在\]
</dt> <dd>

控制作業的旗標。 這個參數可以是 [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa)結構的 *fFlags* 成員下所列的一或多個值。

若是印表機複製勾點，此值是在 shellapi 中定義的下列值之一。

| 值       | 描述 |
|-------------|------------|
|  **PO_DELETE**      | 正在刪除印表機。 *SrcFile* 參數指向指定印表機的完整路徑。           |
|  **PO_RENAME**       | 印表機已重新命名。 *SrcFile* 參數會指向印表機的新名稱。 *DestFile* 參數會指向舊的名稱。           |
| **PO_PORTCHANGE**    | 不支援。 請勿使用。          |
| **PO_REN_PORT**    | 不支援。 請勿使用。           |

</dd> </dl>

<dl> <dt>

*srcFile* \[在\]
</dt> <dd>

包含源資料夾名稱之字串的指標。

</dd> </dl>

*srcAttribs* \[在\]
</dt> <dd>

源資料夾的屬性。 這個參數可以是標頭檔中所定義之任何檔案屬性旗標 (FILE_ATTRIBUTE_ * ) 的組合。 請參閱 [檔案屬性常數](../fileio/file-attribute-constants.md)。

</dd> </dl>

*destFile* \[在\]
</dt> <dd>

包含目的資料夾名稱之字串的指標。

</dd> </dl>

*destAttribs* \[在\]
</dt> <dd>

目的資料夾的屬性。 這個參數可以是標頭檔中所定義之任何檔案屬性旗標 (FILE_ATTRIBUTE_ * ) 的組合。 請參閱 [檔案屬性常數](../fileio/file-attribute-constants.md)。

</dd> </dl>

*結果* \[擴展\]
</dt> <dd>

整數值，指出 Shell 是否應執行作業。 下列其中之一：

| 值       | 描述 |
|-------------|------------|
| **IDYES**       | 允許操作。           |
| **IDNO**        | 防止此資料夾上的作業，但會繼續進行已核准 (例如，批次複製作業) 的任何其他作業。           |
| **IDCANCEL**    | 防止目前的作業，並取消任何暫止的作業。           |


</dd> </dl>


## <a name="return-value"></a>傳回值

如果成功，則傳回 **S_OK** ，否則傳回錯誤碼。

## <a name="remarks"></a>備註

Shell 會針對註冊的同步根目錄下的每個資料夾，呼叫雲端提供者的複製勾點處理常式。 若要註冊雲端資料夾的複製勾點處理常式，請將 **HKEY_LOCAL_MACHINE/software/microsoft/windows/currentversion/explorer/syncrootmanager/{syncrootid}** 機碼底下的 **CopyHook** 值設定為複製攔截物件的 CLSID。

呼叫 **CopyCallback** 方法時，Shell 會直接初始化 [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) 介面，而不會先使用 [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 介面。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 10 Insider Preview 組建19624                                |
| 標頭                   | shobjidl.h。h   |

## <a name="see-also"></a>另請參閱

[建立支援預留位置檔案的雲端同步處理引擎](../cfapi/build-a-cloud-file-sync-engine.md)