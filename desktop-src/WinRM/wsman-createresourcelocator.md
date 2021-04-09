---
title: 'CreateResourceLocator 方法 (WSManDisp .h) '
description: 建立可使用的 ResourceLocator 物件，而不是在會話物件作業中指定資源 URI，例如 Session. Get、Session. Put 或 Session。列舉。
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- CreateResourceLocator 方法 Windows 遠端管理
- CreateResourceLocator 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，CreateResourceLocator 方法
topic_type:
- apiref
api_name:
- WSMan.CreateResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6982d1ea0b257ca9276918931ce233e675fd3eb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934289"
---
# <a name="wsmancreateresourcelocator-method"></a>WSMan. CreateResourceLocator 方法

建立可使用的 [**ResourceLocator**](resourcelocator.md) 物件，而不 [**是在會話物件作業中**](session.md) 指定資源 URI，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**session。列舉**](session-enumerate.md)。

## <a name="syntax"></a>語法


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*uri* \[在中，選擇性\]
</dt> <dd>

資源的資源 URI。 如需 URI 字串的詳細資訊，請參閱 [資源 uri](resource-uris.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

之後可以用來執行本機或遠端 WinRM 作業的 [**ResourceLocator**](resourcelocator.md) 物件。

## <a name="remarks"></a>備註

如果未在 [**ResourceLocator**](resourcelocator.md)物件中指定 **FragmentDialect** 屬性，則預設值為 XPath 1.0 規格。 如需詳細資訊，請參閱 [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath)。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會建立 [**ResourceLocator**](resourcelocator.md)物件，並從索引為 "1" 的 [**Win32 \_ >networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)實例取得網路介面卡 **描述** 屬性值。


```VB
const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
const FragmentPath = "Description"

Set objWSMan = CreateObject("WSMan.Automation")

Set objSession = objWSMan.CreateSession()

Set objLocator = objWSMan.CreateResourceLocator(Uri)

objLocator.AddSelector "Index", "1"
objLocator.FragmentPath = FragmentPath

Dim Xml
Xml = objSession.Get(objLocator)
WScript.Echo Xml
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**工作階段**](session.md)
</dt> </dl>

 

