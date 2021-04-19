---
description: 安裝程式物件的 ProvideAssembly 方法會傳回元件的已安裝路徑。
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: 安裝程式：:P rovideAssembly 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideAssembly
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f81c9ab9b43b814307242cc828326b2b7e7d79fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994852"
---
# <a name="installerprovideassembly-method"></a>安裝程式：:P rovideAssembly 方法

[**安裝程式**](installer-object.md)物件的 **ProvideAssembly** 方法會傳回元件的已安裝路徑。

## <a name="syntax"></a>語法


```JScript
retVal = .ProvideAssembly(
  assembly,
  appContext,
  installMode,
  assemblyInfo
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*裝配* 
</dt> <dd>

要查詢之已安裝元件的強式名稱。

</dd> <dt>

*appCoNtext* 
</dt> <dd>

全域程式集的設為 null。 若為私用元件，請將 *appCoNtext* 設定為應用程式佈建檔的完整路徑，或設定為私用元件之應用程式的可執行檔完整路徑。

</dd> <dt>

*installMode* 
</dt> <dd>

定義安裝模式。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                                                                                                              | 意義                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                                | 提供元件，並執行提供元件所需的任何安裝。 <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>-1</dt> </dl>                                                                                           | 只有在功能存在時，才提供元件。 此選項會確認元件是否存在。<br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt> </dl>                                                                               | 只有在功能存在時，才提供元件。 此選項不會驗證元件是否存在。<br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt> </dl>                                                   | 只有在元件安裝在本機時，才會提供元件。<br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <dt>**ReinstallFeature 所使用之旗標的組合 [](installer-reinstallfeature.md)**</dt> </dl> | 呼叫 [**ReinstallFeature**](installer-reinstallfeature.md) 方法，以使用這個 *ReinstallMode* 參數重新安裝此功能，然後傳回元件路徑。<br/> |



 

</dd> <dt>

*assemblyInfo* 
</dt> <dd>

元件資訊和元件類型。 設定為下列其中一個值。



| 值                                                                                                                                                                                                                                                                                       | 意義                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <dt>**msiProvideAssemblyNet**</dt> <dt>0</dt> </dl>         | .NET 元件。<br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt> </dl> | Win32 並存元件。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

已安裝元件的路徑。

## <a name="remarks"></a>備註

**ProvideAssembly** 方法會使用 [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)函數。

## <a name="examples"></a>範例

下列範例腳本示範如何使用 ProvideAssembly 方法。


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' ProvideAssembly - .NET global
'   
MsgBox Installer.ProvideAssembly("System.Security,Version=""1.0.5000.0"",PublicKeyToken=""b03f5f7f11d50a3a"",Culture=""neutral"",FileVersion=""1.1.4322.573""", vbNullString, 0, 0)

'
' ProvideAssembly - .NET private
'   
MsgBox Installer.ProvideAssembly("Sample,Version=""1.0.0.0"",Culture=""neutral""", "C:\Program Files\Microsoft\Sample\Sample.exe", 0, 0)

'
' ProvideAssembly - win32 global
'
MsgBox Installer.ProvideAssembly("Microsoft.MSXML2,publicKeyToken=""6bd6b9abf345378f"",version=""4.1.0.0"",type=""win32"",processorArchitecture=""x86""", vbNullString , -2, 1)
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

 

 




