---
description: 安裝程式物件的 CreateAdvertiseScript 方法會產生公告腳本。
ms.assetid: 32a331e5-d291-49cd-ab0e-7d0e4d72a95b
title: Installer：： CreateAdvertiseScript 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateAdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9ec4b18eee376e7bde4824a497ea14b503045f43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980246"
---
# <a name="installercreateadvertisescript-method"></a>Installer：： CreateAdvertiseScript 方法

[**安裝程式**](installer-object.md)物件的 **CreateAdvertiseScript** 方法會產生公告腳本。

## <a name="syntax"></a>語法


```JScript
.CreateAdvertiseScript(
  packagePath,
  scriptFilePath,
  transforms,
  language,
  platform,
  options
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*packagePath* 
</dt> <dd>

要公告的 Windows Installer 封裝 ( .msi) 的完整路徑。

</dd> <dt>

*scriptFilePath* 
</dt> <dd>

要以公告的資訊建立之腳本檔案的完整路徑。

</dd> <dt>

*變換* 
</dt> <dd>

要套用至產品的轉換清單。 清單中的轉換會以分號分隔。 這是選擇性參數。

</dd> <dt>

*language* 
</dt> <dd>

要使用之安裝套件的語言。 這是選擇性參數。

</dd> <dt>

*平台* 
</dt> <dd>

此參數會指定安裝程式應建立腳本的平臺。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                                       | 意義                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="msiAdvertiseCurrentPlatform"></span><span id="msiadvertisecurrentplatform"></span><span id="MSIADVERTISECURRENTPLATFORM"></span><dl> <dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt> </dl> | 建立目前平臺的腳本。<br/>  |
| <span id="msiAdvertiseX86Platform"></span><span id="msiadvertisex86platform"></span><span id="MSIADVERTISEX86PLATFORM"></span><dl> <dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt> </dl>                 | 建立 x86 平臺的腳本。<br/>      |
| <span id="msiAdvertiseIA64Platform"></span><span id="msiadvertiseia64platform"></span><span id="MSIADVERTISEIA64PLATFORM"></span><dl> <dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt> </dl>             | 建立 Itanium 型系統的腳本。<br/> |
| <span id="msiAdvertiseX64Platform"></span><span id="msiadvertisex64platform"></span><span id="MSIADVERTISEX64PLATFORM"></span><dl> <dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt> </dl>                 | 建立 x64 平臺的腳本。<br/>      |



 

</dd> <dt>

*options* 
</dt> <dd>

公告選項。 這是選擇性參數。 此參數可以是下列其中一個值。 這是選擇性參數。



| 值                                                                                                                                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <dt>**msiAdvertiseDefault**</dt> <dt>0</dt> </dl>                             | 標準公告<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt> </dl> | 通告產品的新實例。 需要 *轉換* 參數之轉換清單中的第一個轉換是變更產品代碼的實例轉換。 如需詳細資訊，請參閱 [安裝多個產品和修補程式實例](installing-multiple-instances-of-products-and-patches.md)。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

[**AdvertiseProduct**](installer-advertiseproduct.md)方法會使用 [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)函數。

## <a name="examples"></a>範例

下列範例示範如何使用 **CreateAdvertiseScript** 方法。


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Create an advertise script for Orca
'

Installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scripts\orca.aas"
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 和 Windows XP 上的 Windows Installer 4。5<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**安裝程式**](installer-object.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




